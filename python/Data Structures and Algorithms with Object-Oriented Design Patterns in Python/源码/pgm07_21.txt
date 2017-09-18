#
# This file contains the Python code from Program 7.21 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_21.txt
#
class PolynomialAsOrderedList(Polynomial):

    def __init__(self):
        self._list = OrderedListAsLinkedList()

    def addTerm(self, term):
        self._list.insert(term)

    def accept(self, visitor):
        assert isinstance(visitor, Visitor)
        self._list.accept(visitor)

    def find(self, term):
        return self._list.find(term)

    def withdraw(self, term):
        self._list.withdraw(term)

    # ...
