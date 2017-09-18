#
# This file contains the Python code from Program 11.16 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_16.txt
#
class BinomialQueue(MergeablePriorityQueue):

    def getMinTree(self):
        minTree = None
        ptr = self._treeList.head
        while ptr is not None:
            tree = ptr.datum
            if minTree is None or tree.key < minTree.key:
                minTree = tree
            ptr = ptr.next
        return minTree

    minTree = property(
        fget = lambda self: self.getMinTree())

    def getMin(self):
        if self._count == 0:
            raise ContainerEmpty
        return self.minTree.key

    # ...
