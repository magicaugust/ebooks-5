#
# This file contains the Python code from Program 15.16 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_16.txt
#
class BucketSorter(Sorter):

    def __init__(self, m):
        super(BucketSorter, self).__init__()
        self._m = m
        self._count = Array(self._m)

    # ...
}
