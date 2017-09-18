#
# This file contains the Python code from Program 12.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_06.txt
#
class SetAsBitVector(Set):

    BITS = 32 # Number of bits in an integer.

    def __init__(self, n):
        super(SetAsBitVector, self).__init__(n)
        self._vector = Array((n + self.BITS - 1) / self.BITS)
        for i in xrange(len(self._vector)):
            self._vector[i] = 0

    # ...
