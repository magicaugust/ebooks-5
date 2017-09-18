#
# This file contains the Python code from Program 15.18 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_18.txt
#
class RadixSorter(Sorter):

    r = 8
    R = 1 << r
    p = (32 + r - 1) / r

    def __init__(self):
        self._count = Array(self.R)
        self._tempArray = None

    # ...
