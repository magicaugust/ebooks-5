#
# This file contains the Python code from Program 4.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_11.txt
#
class LinkedList(object):

    class Element(object):

        def __init__(self, list, datum, next):
            self._list = list
            self._datum = datum
            self._next = next

        def getDatum(self):
            return self._datum

        datum = property(
            fget = lambda self: self.getDatum())

        def getNext(self):
            return self._next

        next = property(
            fget = lambda self: self.getNext())

    # ...
