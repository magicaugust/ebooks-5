#
# This file contains the Python code from Program 8.2 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_02.txt
#
class Float(float, Object):

    def __hash__(self):
	(m, e) = math.frexp(self)
	mprime = int((abs(m) - 0.5) * (1L << 52))
	return mprime >> 20

    # ...
