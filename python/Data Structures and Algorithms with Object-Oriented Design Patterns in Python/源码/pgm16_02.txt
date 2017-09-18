#
# This file contains the Python code from Program 16.2 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_02.txt
#
class Edge(Object):

    def __init__(self):
        super(Edge, self).__init__()

    def getV0(self): pass
    getV0 = abstractmethod(getV0)
    v0 = property(
        fget = lambda self: self.getV0())

    def getV1(self): pass
    getV1 = abstractmethod(getV1)
    v1 = property(
        fget = lambda self: self.getV1())

    def getWeight(self): pass
    getWeight = abstractmethod(getWeight)
    weight = property(
        fget = lambda self: self.getWeight())

    def getIsDirected(self): pass
    getIsDirected = abstractmethod(getIsDirected)
    isDirected = property(
        fget = lambda self: self.getIsDirected())

    def mateOf(self, vertex): pass
    mateOf = abstractmethod(mateOf)
