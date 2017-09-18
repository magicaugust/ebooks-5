#
# This file contains the Python code from Program 4.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_09.txt
#
class DenseMatrix(Matrix):

    def __init__(self, rows, cols):
        super(DenseMatrix, self).__init__(rows, cols)
        self._array = MultiDimensionalArray(rows, cols)

    def __getitem__(self, (i, j)):
        return self._array[i,j]

    def __setitem__(self, (i, j), value):
        self._array[i,j] = value

    # ...
