#
# This file contains the Python code from Program 7.2 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_02.txt
#
class Cursor(Object):

    def __init__(self, list):
        super(Cursor, self).__init__()
	self._list = list

    def getDatum(self):
        pass
    getDatum = abstractmethod(getDatum)

    datum = property(
        fget = lambda self: self.getDatum())

    def insertAfter(self, obj):
        pass
    insertAfter = abstractmethod(insertAfter)

    def insertBefore(self, obj):
        pass
    insertBefore = abstractmethod(insertBefore)

    def withdraw(self, obj):
        pass
    withdraw = abstractmethod(withdraw)
