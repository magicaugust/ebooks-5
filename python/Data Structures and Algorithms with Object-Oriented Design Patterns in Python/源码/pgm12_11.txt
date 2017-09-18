#
# This file contains the Python code from Program 12.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_11.txt
#
class MultisetAsArray(Multiset):

    def insert(self, item):
        self._array[item] += 1

    def withdraw(self, item):
        if self._array[item] == 0:
            raise KeyEerror
        self._array[item] -= 1

    def __contains__(self, item):
        return self._array[item] > 0

    # ...
