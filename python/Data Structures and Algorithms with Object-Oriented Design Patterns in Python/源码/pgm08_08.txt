#
# This file contains the Python code from Program 8.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_08.txt
#
class ChainedHashTable(HashTable):

    def __init__(self, length):
        super(ChainedHashTable, self).__init__()
        self._array = Array(length)
        for i in xrange(len(self._array)):
            self._array[i] = LinkedList()

    def __len__(self):
        return len(self._array)

    def purge(self):
        for i in xrange(len(self._array)):
            self._array[i].purge()
        self._count = 0
    # ...
