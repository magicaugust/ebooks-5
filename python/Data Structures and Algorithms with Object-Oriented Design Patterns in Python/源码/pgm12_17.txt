#
# This file contains the Python code from Program 12.17 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_17.txt
#
class PartitionAsForest(Partition):

    class PartitionTree(Set, Tree):

        def __init__(self, partition, item):
            super(PartitionAsForest.PartitionTree, self) \
                .__init__(partition._universeSize)
            self._partition = partition
            self._item = item
            self._parent = None
            self._rank = 0
            self._count = 1

        # ...

    # ...
