#
# This file contains the Python code from Program 10.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_06.txt
#
class AVLTree(BinarySearchTree):

    def __init__(self):
        super(AVLTree, self).__init__()
        self._height = -1

    # ...
