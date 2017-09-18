#
# This file contains the Python code from Program 4.17 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_17.txt
#
class LinkedList(object):

    def append(self, item):
        tmp = self.Element(self, item, None)
        if self._head is None:
            self._head = tmp
        else:
            self._tail._next = tmp
        self._tail = tmp

    # ...
