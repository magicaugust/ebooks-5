#
# This file contains the Python code from Program 7.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_03.txt
#
class OrderedListAsArray(OrderedList):

    def __init__(self, size = 0):
        super(OrderedListAsArray, self).__init__()
        self._array = Array(size)

    # ...
