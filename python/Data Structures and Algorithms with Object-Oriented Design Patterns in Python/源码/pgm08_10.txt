#
# This file contains the Python code from Program 8.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_10.txt
#
class ChainedHashTable(HashTable):

    def find(self, obj):
        ptr = self._array[self.h(obj)].head
        while ptr is not None:
            datum = ptr.datum
            if obj == datum:
                return datum
            ptr = ptr.next
        return None
    # ...
