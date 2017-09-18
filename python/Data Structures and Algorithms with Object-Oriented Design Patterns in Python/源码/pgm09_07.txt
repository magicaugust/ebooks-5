#
# This file contains the Python code from Program 9.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_07.txt
#
class Tree(Container):

    def breadthFirstTraversal(self, visitor):
        assert isinstance(visitor, Visitor)
        queue = QueueAsLinkedList()
        if not self.isEmpty:
            queue.enqueue(self)
        while not queue.isEmpty and not visitor.isDone:
            head = queue.dequeue()
            visitor.visit(head.key)
            for i in xrange(head.degree):
                child = head.getSubtree(i)
                if not child.isEmpty:
                    queue.enqueue(child)

    # ...
