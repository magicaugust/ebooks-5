#
# This file contains the Python code from Program 6.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_11.txt
#
class Queue(Container):

    def __init__(self):
        super(Queue, self).__init__()

    def getHead(self):
        pass
    getHead = abstractmethod(getHead)

    head = property(
        fget = lambda self: self.getHead())

    def enqueue(self, obj):
        pass
    enqueue = abstractmethod(enqueue)

    def dequeue(self):
        pass
    dequeue = abstractmethod(dequeue)
