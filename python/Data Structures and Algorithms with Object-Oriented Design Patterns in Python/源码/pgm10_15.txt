#
# This file contains the Python code from Program 10.15 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_15.txt
#
class MWayTree(SearchTree):

    def find(self, obj):
        if self.isEmpty:
            return None
        i = self._count
        while i > 0:
            diff = cmp(obj, self._key[i])
            if diff == 0:
                return self._key[i]
            if diff > 0:
                break
            i = i - 1
        return self._subtree[i].find(obj)

    # ...
