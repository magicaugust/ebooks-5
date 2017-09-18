#
# This file contains the Python code from Program 6.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_01.txt
#
class Stack(Container):

    def __init__(self):
        super(Stack, self).__init__()

    def getTop(self):
        pass
    getTop = abstractmethod(getTop)

    top = property(
        fget = lambda self: self.getTop())

    def push(self, obj):
        pass
    push = abstractmethod(push)

    def pop(self):
        pass
    pop = abstractmethod(pop)
