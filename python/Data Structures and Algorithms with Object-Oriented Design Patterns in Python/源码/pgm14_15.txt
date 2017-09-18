#
# This file contains the Python code from Program 14.15 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_15.txt
#
class UniformRV(RandomVariable):

    def __init__(self, u, v):
        self._u = u;
        self._v = v;

    def getNext(self):
        return self._u + (self._v - self._u) * \
	    RandomNumberGenerator.next
