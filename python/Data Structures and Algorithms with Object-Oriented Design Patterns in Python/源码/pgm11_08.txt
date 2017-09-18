#
# This file contains the Python code from Program 11.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_08.txt
#
class LeftistHeap(BinaryTree, MergeablePriorityQueue):

    def merge(self, queue):
        if self.isEmpty:
            self.swapContentsWith(queue)
        elif not queue.isEmpty:
            if self._key > queue._key:
                self.swapContentsWith(queue)
            self._right.merge(queue)
            if self._left._nullPathLength \
                    < self._right._nullPathLength:
                self.swapSubtrees()
            self._nullPathLength = 1 + min(
                self._left._nullPathLength,
                self._right._nullPathLength)

    # ...
