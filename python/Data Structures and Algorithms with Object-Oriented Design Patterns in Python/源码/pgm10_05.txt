#
# This file contains the Python code from Program 10.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_05.txt
#
class BinarySearchTree(BinaryTree, SearchTree):

    def withdraw(self, obj):
        if self.isEmpty:
            raise KeyError
        diff = cmp(obj, self._key)
        if diff == 0:
            if not self._left.isEmpty:
                max = self._left.max
                self._key = max
                self._left.withdraw(max)
            elif not self._right.isEmpty:
                min = self._right.min
                self._key = min
                self._right.withdraw(min)
            else:
                self.detachKey()
        elif diff < 0:
            self._left.withdraw(obj)
        elif diff > 0:
            self._right.withdraw(obj)
        self.balance()

    # ...
