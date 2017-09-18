#
# This file contains the Python code from Program 15.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_13.txt
#
class TwoWayMergeSorter(Sorter):

    def __init__(self):
        super(TwoWayMergeSorter, self).__init__()
        self._tempArray = None

    # ...
