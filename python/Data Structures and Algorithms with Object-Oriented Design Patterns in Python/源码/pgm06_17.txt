#
# This file contains the Python code from Program 6.17 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_17.txt
#
class Deque(Queue):

    def __init__(self):
        super(Deque, self).__init__()

    def getHead(self):
        pass
    getHead = abstractmethod(getHead)

    head = property(
        fget = lambda self: self.getHead())

    def getTail(self):
        pass
    getTail = abstractmethod(getTail)

    tail = property(
        fget = lambda self: self.getTail())

    def enqueueHead(self, obj):
        pass
    enqueueHead = abstractmethod(enqueueHead)

    def dequeueHead(self):
        return self.dequeue()

    def enqueueTail(self, object):
        self.enqueue(object)

    def dequeueTail(self):
        pass
    dequeueTail = abstractmethod(dequeueTail)
