#
# This file contains the Python code from Program 7.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_10.txt
#
class OrderedListAsArray(OrderedList):

    class Cursor(Cursor):

        def withdraw(self):
            if self._offset < 0 \
                    or self._offset >= self._list._count:
                raise IndexError
            if self._list._count == 0:
                raise ContainerEmpty
            i = self._offset
            while i < self._list._count - 1:
                self._list._array[i] = self._list._array[i + 1]
                i += 1
                ++i
            self._list._array[i] = None
            self._list._count -= 1

        # ...

    # ...
