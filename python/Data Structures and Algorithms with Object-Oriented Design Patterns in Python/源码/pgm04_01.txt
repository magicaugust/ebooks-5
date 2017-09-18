#
# This file contains the Python code from Program 4.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_01.txt
#
class Array(object):

    def __init__(self, length = 0, baseIndex = 0):
	assert length >= 0
        self._data = [ None for i in xrange(length) ]
        self._baseIndex = baseIndex

    # ...
