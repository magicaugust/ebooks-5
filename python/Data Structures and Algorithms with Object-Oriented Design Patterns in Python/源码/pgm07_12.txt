#
# This file contains the Python code from Program 7.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_12.txt
#
class OrderedListAsLinkedList(OrderedList):

    def insert(self, obj):
        self._linkedList.append(obj)
        self._count += 1

    def __getitem__(self, offset):
        if offset < 0 or offset >= self._count:
            raise IndexError
        ptr = self._linkedList.head
        i = 0
        while i < offset and ptr is not None:
            ptr = ptr.next
            i += 1
        return ptr.datum

    # ...
