#
# This file contains the Python code from Program 16.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_06.txt
#
class Digraph(Graph):

    def __init__(self, size):
        super(Digraph, self).__init__(size)
        self._isDirected = True

    def getIsStronglyConnected(self): pass
    getIsStronglyConnected = abstractmethod(
        getIsStronglyConnected)
    isStronglyConnected = property(
        fget = lambda self: self.getIsStronglyConnected())

    def topologicalOrderTraversal(self): pass
    topologicalOrderTraversal = abstractmethod(
        topologicalOrderTraversal)

    # ...
