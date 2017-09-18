#
# This file contains the Python code from Program 6.16 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_16.txt
#
class Algorithms(object):

    def breadthFirstTraversal(tree):
        queue = QueueAsLinkedList()
        queue.enqueue(tree)
        while not queue.isEmpty:
            t = queue.dequeue()
            print t.key
            for i in xrange(t.degree):
                subTree = t.getSubtree(i)
		queue.enqueue(subTree)
    breadthFirstTraversal = staticmethod(breadthFirstTraversal)
