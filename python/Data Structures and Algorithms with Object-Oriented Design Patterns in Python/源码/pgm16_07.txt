#
# This file contains the Python code from Program 16.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_07.txt
#
class GraphAsMatrix(Graph):

    def __init__(self, size):
        super(GraphAsMatrix, self).__init__(size)
        self._matrix = DenseMatrix(size, size)

    # ...
