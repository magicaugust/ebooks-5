#
# This file contains the Python code from Program A.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm0A_05.txt
#
class Complex(object):

    def __add__(self, c):
        return Complex(self.real + c.real, self.imag + c.imag)

    def __sub__(self, c):
        return Complex(self.real - c.real, self.imag - c.imag)

    def __mul__(self, c):
	return Complex(self.real * c.real - self.imag * c.imag,
	    self.real * c.imag + self.imag * c.real)

    # ...
