#
# This file contains the Python code from Program 16.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_04.txt
#
class Graph(Container):

    def getNumberOfEdges(self): pass
    getNumberOfEdges = abstractmethod(getNumberOfEdges)
    numberOfEdges = property(
        fget = lambda self: self.getNumberOfEdges())

    def getNumberOfVertices(self): pass
    getNumberOfVertices = abstractmethod(getNumberOfVertices)
    numberOfVertices = property(
        fget = lambda self: self.getNumberOfVertices())

    def getIsDirected(self): pass
    getIsDirected = abstractmethod(getIsDirected)
    isDirected = property(
        fget = lambda self: self.getIsDirected())

    def getIsConnected(self): pass
    getIsConnected = abstractmethod(getIsConnected)
    isConnected = property(
        fget = lambda self: self.getIsConnected())

    def getIsCyclic(self): pass
    getIsCyclic = abstractmethod(getIsCyclic)
    isCyclic = property(
        fget = lambda self: self.getIsCyclic())

    def getVertices(self): pass
    getVertices = abstractmethod(getVertices)
    vertices = property(
        fget = lambda self: self.getVertices())

    def getEdges(self): pass
    getEdges = abstractmethod(getEdges)
    edges = property(
        fget = lambda self: self.getEdges())

    # ...
