#
# This file contains the Python code from Program 11.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_13.txt
#
class BinomialQueue(MergeablePriorityQueue):

    class BinomialTree(GeneralTree):

        def add(self, tree):
            if self._degree != tree._degree:
                raise ValueError
            if self._key > tree._key:
                self.swapContentsWith(tree)
            self.attachSubtree(tree)
            return self

        # ...

    # ...
