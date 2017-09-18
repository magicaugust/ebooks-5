#
# This file contains the Python code from Program 10.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_10.txt
#
class AVLTree(BinarySearchTree):

    def balance(self):
        self.adjustHeight()
        if self.balanceFactor > 1:
            if self._left.balanceFactor > 0:
                self.doLLRotation()
            else:
                self.doLRRotation()
        elif self.balanceFactor < -1:
            if self._right.balanceFactor < 0:
                self.doRRRotation()
            else:
                self.doRLRotation()

    # ...
