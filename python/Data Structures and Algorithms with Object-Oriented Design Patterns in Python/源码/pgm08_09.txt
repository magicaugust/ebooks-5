#
# This file contains the Python code from Program 8.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_09.txt
#
class ChainedHashTable(HashTable):

    def insert(self, obj):
        self._array[self.h(obj)].append(obj)
        self._count += 1

    def withdraw(self, obj):
        self._array[self.h(obj)].extract(obj)
        self._count -= 1
    # ...
