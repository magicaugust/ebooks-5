#
# This file contains the Python code from Program 10.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_12.txt
#
class AVLTree(BinarySearchTree):

    def detachKey(self):
        self._height = -1
        return super(AVLTree, self).detachKey()

    # ...
