#
# This file contains the Python code from Program 4.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_08.txt
#
class Matrix(object):

    def __init__(self, numberOfRows, numberOfColumns):
	assert numberOfRows >= 0
	assert numberOfColumns >= 0
        super(Matrix, self).__init__()
        self._numberOfRows = numberOfRows
        self._numberOfColumns = numberOfColumns

    def getNumberOfRows(self):
        return self._numberOfRows

    numberOfRows = property(
        fget = lambda self: self.getNumberOfRows())

    def getNumberOfColumns(self):
        return self._numberOfColumns

    numberOfColumns = property(
        fget = lambda self: self.getNumberOfColumns())

    # ...
