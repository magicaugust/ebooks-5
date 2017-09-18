#
# This file contains the Python code from Program 7.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_07.txt
#
class OrderedListAsArray(OrderedList):

    class Cursor(Cursor):

        def __init__(self, list, offset):
	    super(OrderedListAsArray.Cursor, self).__init__(list)
            self._offset = offset

        def getDatum(self):
            if self._offset < 0 \
                    or self._offset >= self._list._count:
                raise IndexError
            return self._list._array[self._offset]

        # ...

    # ...
