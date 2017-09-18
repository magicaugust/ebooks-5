#
# This file contains the Python code from Program A.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm0A_04.txt
#
class Complex(object):

    def getR(self):
        return math.sqrt(self._real * self._real
	    + self._imag * self._imag)

    def setR(self, value):
        theta = self.theta
        self._real = value * math.cos(theta)
        self._imag = value * math.sin(theta)

    r = property(
        fget = getR,
        fset = setR)

    def getTheta(self):
        return math.atan2(self._imag, self._real)

    def setTheta(self, value):
        r = self.r
        self._real = r * math.cos(value)
        self._imag = r * math.sin(value)

    theta = property(
        fget = getTheta,
        fset = setTheta)

    # ...
