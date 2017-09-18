#
# This file contains the Python code from Program 12.19 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_19.txt
#
class PartitionAsForest(Partition):

    def find(self, item):
        ptr = self._array[item]
        while ptr._parent is not None:
            ptr = ptr._parent
        return ptr

    # ...
