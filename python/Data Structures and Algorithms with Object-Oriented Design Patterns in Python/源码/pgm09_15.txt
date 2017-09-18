#
# This file contains the Python code from Program 9.15 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_15.txt
#
class BinaryTree(Tree):

    def __init__(self, *args):
        super(BinaryTree, self).__init__()
        if len(args) == 0:
            self._key = None
            self._left = None
            self._right = None
        elif len(args) == 1:
            self._key = args[0]
            self._left = BinaryTree()
            self._right = BinaryTree()
        elif len(args) == 3:
            self._key = args[0]
            self._left = args[1]
            self._right = args[2]
        else:
            raise ValueError

    def purge(self):
        self._key = None
        self._left = None
        self._right = None

    # ...
