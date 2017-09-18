#
# This file contains the Python code from Program 6.2 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_02.txt
#
class StackAsArray(Stack):

    def __init__(self, size = 0):
        super(StackAsArray, self).__init__()
        self._array = Array(size)

    def purge(self):
        while self._count > 0:
            self._array[self._count] = None
            self._count -= 1

    #...
