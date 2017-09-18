#
# This file contains the Python code from Program 12.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_01.txt
#
class Set(SearchableContainer):

    def __init__(self, universeSize):
        self._universeSize = universeSize

    def getUniverseSize(self):
        return self._universeSize

    universeSize = property(
        fget = lambda self: self.getUniverseSize())

    def __or__(self, set):
        pass
    __or__ = abstractmethod(__or__)

    def __and__(self, set):
        pass
    __and__ = abstractmethod(__and__)

    def __sub__(self, set):
        pass
    __sub__ = abstractmethod(__sub__)

    def __eq__(self, set):
        pass
    __eq__ = abstractmethod(__eq__)

    def __lt__(self, set):
        pass
    __lt__ = abstractmethod(__lt__)
