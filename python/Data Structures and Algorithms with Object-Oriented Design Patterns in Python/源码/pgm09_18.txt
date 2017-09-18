#
# This file contains the Python code from Program 9.18 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_18.txt
#
class BinaryTree(Tree):

    def _compareTo(self, bt):
        assert isinstance(self, bt.__class__)
        if self.isEmpty:
            if bt.isEmpty:
                return 0
            else:
                return -1
        elif bt.isEmpty:
            return 1
        else:
            result = cmp(self._key, bt._key)
            if result == 0:
                result = cmp(self._left, bt._left)
            if result == 0:
                result = cmp(self._right, bt._right)
            return result

    # ...
