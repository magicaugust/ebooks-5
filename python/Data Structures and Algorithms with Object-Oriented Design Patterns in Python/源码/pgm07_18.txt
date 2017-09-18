#
# This file contains the Python code from Program 7.18 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_18.txt
#
class OrderedListAsLinkedList(OrderedList):

    class Cursor(Cursor):

        def withdraw(self):
            self._list._linkedList.extract(self._element.datum)
            self._list._count -= 1

        # ...

    # ...
