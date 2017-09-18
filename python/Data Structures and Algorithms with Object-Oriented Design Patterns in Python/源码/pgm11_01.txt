#
# This file contains the Python code from Program 11.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_01.txt
#
class PriorityQueue(Container):

    def __init__(self):
        super(PriorityQueue, self).__init__()

    def enqueue(self, obj):
        pass
    enqueue = abstractmethod(enqueue)

    def getMin(self):
        pass
    getMin = abstractmethod(getMin)

    min = property(
        fget = lambda self: self.getMin())

    def dequeueMin(self):
        pass
    dequeueMin = abstractmethod(dequeueMin)
