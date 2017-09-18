#
# This file contains the Python code from Program 10.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_03.txt
#
class BinarySearchTree(BinaryTree, SearchTree):

    def find(self, obj):
        if self.isEmpty:
            return None
        diff = cmp(obj, self._key)
        if diff == 0:
            return self._key
        elif diff < 0:
            return self._left.find(obj)
        elif diff > 0:
            return self._right.find(obj)

    def getMin(self):
        if self.isEmpty:
            return None
        elif self._left.isEmpty:
            return self._key
        else:
            return self._left.min

    # ...
