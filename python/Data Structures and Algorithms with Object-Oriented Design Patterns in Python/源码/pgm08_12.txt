#
# This file contains the Python code from Program 8.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_12.txt
#
class ChainedScatterTable(HashTable):

    def __init__(self, length):
        super(ChainedScatterTable, self).__init__()
        self._array = Array(length)
        for i in xrange(len(self._array)):
            self._array[i] = self.Entry(None, self.NULL)

    def __len__(self):
        return len(self._array)

    def purge(self):
        for i in len(self):
            self._array[i] = self.Entry(None, self.NULL)
        self._count = 0

    # ...
