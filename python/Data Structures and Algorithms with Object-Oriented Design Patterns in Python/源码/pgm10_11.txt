#
# This file contains the Python code from Program 10.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_11.txt
#
class AVLTree(BinarySearchTree):

    def attachKey(self, obj):
        if not self.isEmpty:
            raise StateError
        self._key = obj
        self._left = AVLTree()
        self._right = AVLTree()
        self._height = 0

    # ...
