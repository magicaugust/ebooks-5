#
# This file contains the Python code from Program 10.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_09.txt
#
class AVLTree(BinarySearchTree):

    def doLRRotation(self):
        if self.isEmpty:
            raise StateError
        self._left.doRRRotation()
        self.doLLRotation()

    # ...
