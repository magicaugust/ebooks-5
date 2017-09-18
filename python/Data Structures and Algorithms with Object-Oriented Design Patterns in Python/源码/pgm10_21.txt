#
# This file contains the Python code from Program 10.21 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_21.txt
#
class BTree(MWayTree):

    def insertUp(self, obj, child):
        index = self.findIndex(obj)
        if not self.isFull:
	    self.insertPair(index + 1, obj, child)
            self._count = self._count + 1
        else:
            (extraKey, extraTree) = self.insertPair(
		index + 1, obj, child)
            if self._parent is None:
                left = BTree(self.m)
                right = BTree(self.m)
                left.attachLeftHalfOf(self)
                right.attachRightHalfOf(self)
                right.insertUp(extraKey, extraTree)
                self.attachSubtree(0, left)
                self._key[1] = self._key[(self.m + 1)/2]
                self.attachSubtree(1, right)
                self._count = 1
            else:
                self._count = (self.m + 1)/2 - 1
                right = BTree(self.m)
                right.attachRightHalfOf(self)
                right.insertUp(extraKey, extraTree)
                self._parent.insertUp(
                    self._key[(self.m + 1)/2], right)

    # ...
