#
# This file contains the Python code from Program 4.16 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_16.txt
#
class LinkedList(object):

    def prepend(self, item):
        tmp = self.Element(self, item, self._head)
        if self._head is None:
            self._tail = tmp
        self._head = tmp

    # ...
