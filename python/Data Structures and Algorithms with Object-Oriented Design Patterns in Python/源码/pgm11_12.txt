#
# This file contains the Python code from Program 11.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_12.txt
#
class BinomialQueue(MergeablePriorityQueue):

    class BinomialTree(GeneralTree):

        def __init__(self, key):
            super(BinomialQueue.BinomialTree, self).__init__(key)

        # ...

    # ...
