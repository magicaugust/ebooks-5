#
# This file contains the Python code from Program 10.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_08.txt
#
class AVLTree(BinarySearchTree):

    def doLLRotation(self):
        if self.isEmpty:
            raise StateError
        tmp = self._right
        self._right = self._left
        self._left = self._right._left
        self._right._left = self._right._right
        self._right._right = tmp

        tmp = self._key
        self._key = self._right._key
        self._right._key = tmp

        self._right.adjustHeight()
        self.adjustHeight()

    # ...
