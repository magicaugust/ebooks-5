#
# This file contains the Python code from Program 5.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_09.txt
#
class SearchableContainer(Container):

    def __init__(self):
        super(SearchableContainer, self).__init__()

    def __contains__(self, obj):
        pass
    __contains__ = abstractmethod(__contains__)

    def insert(self, obj):
        pass
    insert = abstractmethod(insert)

    def withdraw(self, obj):
        pass
    withdraw = abstractmethod(withdraw)

    def find(self, obj):
        pass
    find = abstractmethod(find)
