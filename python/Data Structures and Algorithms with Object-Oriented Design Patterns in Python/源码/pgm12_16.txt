#
# This file contains the Python code from Program 12.16 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_16.txt
#
class Partition(Set):

    def __init__(self, n):
        super(Partition, self).__init__(n)

    def find(self, obj):
        pass
    find = abstractmethod(find)

    def join(self, s, t):
        pass
    join = abstractmethod(join)
