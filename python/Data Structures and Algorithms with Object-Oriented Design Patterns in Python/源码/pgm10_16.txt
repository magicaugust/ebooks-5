#
# This file contains the Python code from Program 10.16 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_16.txt
#
class MWayTree(SearchTree):

    def findIndex(self, obj):
        if self.isEmpty or obj < self._key[1]:
            return 0
        left = 1
        right = self._count
        while left < right:
            middle = (left + right + 1) / 2
            if obj < self._key[middle]:
                right = middle - 1
            else:
                left = middle
        return left

    def find(self, obj):
        if self.isEmpty:
            return None
        index = self.findIndex(obj)
        if index != 0 and self._key[index] == obj:
            return self._key[index]
        else:
            return self._subtree[index].find(obj)

    # ...
