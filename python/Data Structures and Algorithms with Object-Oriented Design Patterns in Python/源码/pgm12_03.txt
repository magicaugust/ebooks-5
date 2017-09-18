#
# This file contains the Python code from Program 12.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_03.txt
#
class SetAsArray(Set):

    def insert(self, item):
        self._array[item] = True

    def __contains__(self, item):
        return self._array[item]

    def withdraw(self, item):
        self._array[item] = False

    # ...
