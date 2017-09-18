#
# This file contains the Python code from Program 12.21 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_21.txt
#
class PartitionAsForestV2(PartitionAsForest):

    def find(self, item):
        root = self._array[item]
        while root._parent is not None:
            root = root._parent
        ptr = self._array[item]
        while ptr._parent is not None:
            tmp = ptr._parent
            ptr._parent = root
            ptr = tmp
        return root

    # ...
