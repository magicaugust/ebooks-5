#
# This file contains the Python code from Program 11.20 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_20.txt
#
class BinomialQueue(MergeablePriorityQueue):

    def dequeueMin(self):
        if self._count == 0:
            raise ContainerEmpty
        minTree = self.minTree
        self.removeTree(minTree)
        queue = BinomialQueue()
        while minTree.degree > 0:
            child = minTree.getSubtree(0)
            minTree.detachSubtree(child)
            queue.addTree(child)
        self.merge(queue)
        return minTree.key

    # ...
