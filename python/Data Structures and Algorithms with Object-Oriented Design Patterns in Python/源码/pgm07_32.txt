#
# This file contains the Python code from Program 7.32 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_32.txt
#
class PolynomialAsSortedList(Polynomial):

    def __init__(self):
        super(PolynomialAsSortedList, self).__init__()
        self._list = SortedListAsLinkedList()

    def nextTerm(self, iter):
        try:
            return iter.next()
        except StopIteration:
            return None

    def __add__(self, poly):
        result = PolynomialAsSortedList()
        p1 = iter(self._list)
        p2 = iter(poly._list)
        term1 = self.nextTerm(p1)
        term2 = self.nextTerm(p2);
        while term1 is not None and term2 is not None:
            if term1.exponent < term2.exponent:
                result.addTerm(copy(term1))
                term1 = self.nextTerm(p1)
            elif term1.exponent > term2.exponent:
                result.addTerm(copy(term2))
                term2 = self.nextTerm(p2)
            else:
                sum = term1 + term2
                if sum.coefficient != 0:
                    result.addTerm(sum)
                term1 = self.nextTerm(p1)
                term2 = self.nextTerm(p2)
        while term1 is not None:
            result.addTerm(copy(term1))
            term1 = self.nextTerm(p1)
        while term2 is not None:
            result.addTerm(copy(term2))
            term2 = self.nextTerm(p2)
        return result

    # ...
