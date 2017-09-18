#
# This file contains the Python code from Program 7.31 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_31.txt
#
class Polynomial(Container):

    class Term(Object):

        def __copy__(self):
            return Polynomial.Term(
                self._coefficient, self._exponent)

        def getCoefficient(self):
            return self._coefficient

        coefficient = property(
            fget = lambda self: self.getCoefficient())

        def getExponent(self):
            return self._exponent

        exponent = property(
            fget = lambda self: self.getExponent())

        def __add__(self, term):
	    assert self._exponent == term._exponent
            return Polynomial.Term(
                self._coefficient + term._coefficient,
                self._exponent)

        # ...

    # ...
