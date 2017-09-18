#
# This file contains the Python code from Program 7.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_01.txt
#
class OrderedList(SearchableContainer):

    def __init__(self):
        super(OrderedList, self).__init__()

    def __getitem__(self, i):
        pass
    __getitem__ = abstractmethod(__getitem__)

    def findPosition(self, obj):
        pass
    findPosition = abstractmethod(findPosition)
