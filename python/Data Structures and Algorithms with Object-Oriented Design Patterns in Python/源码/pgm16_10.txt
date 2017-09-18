#
# This file contains the Python code from Program 16.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_10.txt
#
class Graph(Container):

    def breadthFirstTraversal(self, visitor, start):
        assert isinstance(visitor, Visitor)
        enqueued = Array(self._numberOfVertices)
        for v in xrange(self._numberOfVertices):
            enqueued[v] = False
        queue = QueueAsLinkedList()
        queue.enqueue(self[start])
        enqueued[start] = True
        while not queue.isEmpty and not visitor.isDone:
            v = queue.dequeue()
            visitor.visit(v)
            for to in v.successors:
                if not enqueued[to.number]:
                    queue.enqueue(to)
                    enqueued[to.number] = True

    # ...
