#
# This file contains the Python code from Program 7.27 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_27.txt
#
class SortedListAsArray(OrderedListAsArray, SortedList):

    def find(self, obj):
        offset = self.findOffset(obj)
        if offset >= 0:
            return self._array[offset]
        else:
            return None

    class Cursor(OrderedListAsArray.Cursor):

        def __init__(self, list, offset):
            super(SortedListAsArray.Cursor, self) \
                .__init__(list, offset)

        def insertAfter(self, obj):
            raise TypeError

        def insertBefore(self, obj):
            raise TypeError

    def findPosition(self, obj):
        return self.Cursor(self, self.findOffset(obj))

    # ...
