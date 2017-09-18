#
# This file contains the Python code from Program 14.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_13.txt
#
class RandomVariable(Object):

    def __init__(self):
        super(RandomVariable, self).__init__()

    def getNext(self):
        pass
    getNext = abstractmethod(getNext)

    next = property(
        fget = lambda self: self.getNext())
