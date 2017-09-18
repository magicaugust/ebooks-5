#
# This file contains the Python code from Program 11.15 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_15.txt
#
class BinomialQueue(MergeablePriorityQueue):

    def addTree(self, tree):
        self._treeList.append(tree)
        self._count += tree.count

    def removeTree(self, tree):
        self._treeList.extract(tree)
        self._count -= tree.count

    # ...
