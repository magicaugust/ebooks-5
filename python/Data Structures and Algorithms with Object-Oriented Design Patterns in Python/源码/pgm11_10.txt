#
# This file contains the Python code from Program 11.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_10.txt
#
class LeftistHeap(BinaryTree, MergeablePriorityQueue):

    def getMin(self):
        if self.isEmpty:
            raise ContainerEmpty
        return self._key

    # ...
