#
# This file contains the Python code from Program 7.14 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_14.txt
#
class OrderedListAsLinkedList(OrderedList):

    def withdraw(self, obj):
        if self._count == 0:
            raise ContainerEmpty
        self._linkedList.extract(obj)
        self._count -= 1

    # ...
