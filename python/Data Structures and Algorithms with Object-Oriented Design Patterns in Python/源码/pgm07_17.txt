#
# This file contains the Python code from Program 7.17 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_17.txt
#
class OrderedListAsLinkedList(OrderedList):

    class Cursor(Cursor):

        def insertAfter(self, obj):
            self._element.insertAfter(obj)
            self._list._count += 1

        # ...

    # ...
