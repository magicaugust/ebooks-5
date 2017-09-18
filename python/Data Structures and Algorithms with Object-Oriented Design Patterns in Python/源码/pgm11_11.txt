#
# This file contains the Python code from Program 11.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_11.txt
#
class LeftistHeap(BinaryTree, MergeablePriorityQueue):

    def dequeueMin(self):
        if self.isEmpty:
            raise ContainerEmpty
        result = self._key
        oldLeft = self._left
        oldRight = self._right
        self.purge()
        self.swapContentsWith(oldLeft)
        self.merge(oldRight)
        return result

    # ...
