#
# This file contains the Python code from Program 12.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_07.txt
#
class SetAsBitVector(Set):

    def insert(self, item):
        self._vector[item / self.BITS] |= 1 << item % self.BITS

    def withdraw(self, item):
        self._vector[item / self.BITS] &= \
            ~(1 << item % self.BITS)

    def __contains__(self, item):
        return (self._vector[item / self.BITS] \
            & (1 << item % self.BITS)) != 0

    # ...
