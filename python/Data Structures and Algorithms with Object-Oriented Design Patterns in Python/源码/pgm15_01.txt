#
# This file contains the Python code from Program 15.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_01.txt
#
class Sorter(Object):

    def __init__(self):
        super(Sorter, self).__init__()
        self._array = None
        self._n = 0

    def _sort(self):
        pass
    _sort = abstractmethod(_sort)

    def sort(self, array):
        assert isinstance(array, Array)
        self._array = array
        self._n = len(array)
        if self._n > 0:
            self._sort()
        self._array = None

    def swap(self, i, j):
        tmp = self._array[i]
        self._array[i] = self._array[j]
        self._array[j] = tmp
