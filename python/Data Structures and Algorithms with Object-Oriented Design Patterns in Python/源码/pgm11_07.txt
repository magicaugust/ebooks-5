#
# This file contains the Python code from Program 11.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_07.txt
#
class LeftistHeap(BinaryTree, MergeablePriorityQueue):

    def __init__(self, *args):
        if len(args) == 0:
            super(LeftistHeap, self).__init__()
            self._nullPathLength = 0
        else:
            super(LeftistHeap, self).__init__(
                args[0], LeftistHeap(), LeftistHeap())
            self._nullPathLength = 1

    # ...
