#
# This file contains the Python code from Program 12.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_09.txt
#
class Multiset(Set):

    def __init__(self, universeSize):
        super(Multiset, self).__init__(universeSize)
