#
# This file contains the Python code from Program 9.16 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_16.txt
#
class BinaryTree(Tree):

    def getLeft(self):
        if self.isEmpty:
            raise StateError
        return self._left

    left = property(
        fget = lambda self: self.getLeft())

    def getRight(self):
        if self.isEmpty:
            raise StateError
        return self._right

    right = property(
        fget = lambda self: self.getRight())

    # ...
