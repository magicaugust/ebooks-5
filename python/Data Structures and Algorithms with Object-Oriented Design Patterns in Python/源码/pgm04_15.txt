#
# This file contains the Python code from Program 4.15 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_15.txt
#
class LinkedList(object):

    def getFirst(self):
        if self._head is None:
            raise ContainerEmpty
        return self._head._datum

    first = property(
        fget = lambda self: self.getFirst())

    def getLast(self):
        if self._tail is None:
            raise ContainerEmpty
        return self._tail._datum

    last = property(
        fget = lambda self: self.getLast())

    # ...
