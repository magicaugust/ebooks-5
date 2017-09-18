#
# This file contains the Python code from Program 10.20 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_20.txt
#
class BTree(MWayTree):

    def insert(self, obj):
        if self.isEmpty:
            if self._parent is None:
                self.attachSubtree(0, BTree(self.m))
                self._key[1] = obj
                self.attachSubtree(1, BTree(self.m))
                self._count = 1
            else:
                self._parent.insertUp(obj, BTree(self.m))
        else:
            index = self.findIndex(obj)
            if index != 0 and self._key == obj:
                raise KeyError
            self._subtree[index].insert(obj)

    # ...
