#
# This file contains the Python code from Program 9.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_01.txt
#
class Tree(Container):

    def getKey(self):
        pass
    getKey = abstractmethod(getKey)

    key = property(
        fget = lambda self: self.getKey())

    def getSubtree(self, i):
        pass
    getSubtree = abstractmethod(getSubtree)

    def getIsLeaf(self):
        pass
    getIsLeaf = abstractmethod(getIsLeaf)

    isLeaf = property(
        fget = lambda self: self.getIsLeaf())

    def getDegree(self):
        pass
    getDegree = abstractmethod(getDegree)

    degree = property(
        fget = lambda self: self.getDegree())

    def getHeight(self):
        pass
    getHeight = abstractmethod(getHeight)

    height = property(
        fget = lambda self: self.getHeight())

    # ...
