#
# This file contains the Python code from Program 4.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_10.txt
#
class DenseMatrix(Matrix):

    def __mul__(self, mat):
        assert self.numberOfColumns == mat.numberOfRows
        result = DenseMatrix(
            self.numberOfRows, mat.numberOfColumns)
        for i in xrange(self.numberOfRows):
            for j in xrange(mat.numberOfColumns):
                sum = 0
                for k in xrange(self.numberOfColumns):
                    sum += self[i,k] * mat[k,j]
                result[i,j] = sum
        return result

    # ...
