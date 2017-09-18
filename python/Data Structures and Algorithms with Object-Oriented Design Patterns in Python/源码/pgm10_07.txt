#
# This file contains the Python code from Program 10.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_07.txt
#
class AVLTree(BinarySearchTree):

    def getHeight(self):
        return self._height

    def adjustHeight(self):
        if self.isEmpty:
            self._height = -1
        else:
            self._height = 1 + max(
                self._left._height, self._right._height)

    def getBalanceFactor(self):
        if self.isEmpty:
            return 0
        else:
            return self._left._height - self._right._height

    balanceFactor = property(
        fget = lambda self: self.getBalanceFactor())

    # ...
