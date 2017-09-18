#
# This file contains the Python code from Program 4.20 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_20.txt
#
class LinkedList(object):

    class Element(object):

        def insertAfter(self, item):
            self._next = LinkedList.Element(
                self._list, item, self._next)
            if self._list._tail is self:
                self._list._tail = self._next

        def insertBefore(self, item):
            tmp = LinkedList.Element(self._list, item, self)
            if self is self._list._head:
                self._list._head = tmp
            else:
                prevPtr = self._list._head
                while prevPtr is not None \
                        and prevPtr._next is not self:
                    prevPtr = prevPtr._next
                prevPtr._next = tmp

    # ...
