#
# This file contains the Python code from Program 4.19 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_19.txt
#
class LinkedList(object):

    def extract(self, item):
        ptr = self._head
        prevPtr = None
        while ptr is not None and ptr._datum is not item:
            prevPtr = ptr
            ptr = ptr._next
        if ptr is None:
            raise KeyError
        if ptr == self._head:
            self._head = ptr._next
        else:
            prevPtr._next = ptr._next
        if ptr == self._tail:
            self._tail = prevPtr

    # ...
