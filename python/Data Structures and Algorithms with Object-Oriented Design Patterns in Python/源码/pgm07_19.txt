#
# This file contains the Python code from Program 7.19 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_19.txt
#
class Polynomial(Container):

    class Term(Object):

        def __init__(self, coefficient, exponent):
            self._coefficient = coefficient
            self._exponent = exponent

        def _compareTo(self, term):
            assert isinstance(self, term.__class__)
            if self._exponent == term._exponent:
		return cmp(self._coefficient, term._coefficient)
            else:
		return cmp(self._exponent, term._exponent)

        def differentiate(self):
            if self._exponent > 0:
                self._coefficient *= self._exponent
                self._exponent -= 1
            else:
                self._coefficient = 0

        # ...

    # ...
