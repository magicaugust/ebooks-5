#
# This file contains the Python code from Program 7.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_05.txt
#
class OrderedListAsArray(OrderedList):

    def __contains__(self, obj):
        for i in xrange(self._count):
            if self._array[i] is obj:
                return True
        return False

    def find(self, obj):
        for i in xrange(self._count):
            if self._array[i] == obj:
                return self._array[i]
        return None

    # ...
