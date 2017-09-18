#
# This file contains the Python code from Program 5.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_11.txt
#
class Association(Object):

    def getKey(self):
        return self._tuple[0]

    key = property(
        fget = lambda self: self.getKey())

    def getValue(self):
        return self._tuple[1]

    value = property(
        fget = lambda self: self.getValue())

    # ...
