#
# This file contains the Python code from Program 4.14 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_14.txt
#
class LinkedList(object):

    def getHead(self):
        return self._head

    head = property(
        fget = lambda self: self.getHead())
    
    def getTail(self):
        return self._tail

    tail = property(
        fget = lambda self: self.getTail())
    
    def getIsEmpty(self):
        return self._head is None

    isEmpty = property(
        fget = lambda self: self.getIsEmpty())

    # ...
