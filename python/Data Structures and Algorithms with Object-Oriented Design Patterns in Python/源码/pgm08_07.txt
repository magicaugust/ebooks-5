#
# This file contains the Python code from Program 8.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_07.txt
#
class HashTable(SearchableContainer):

    def f(self, obj):
        return hash(obj)

    def g(self, x):
        return abs(x) % len(self)

    def h(self, obj):
        return self.g(self.f(obj))

    # ...
