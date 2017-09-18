#
# This file contains the Python code from Program 11.2 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_02.txt
#
class MergeablePriorityQueue(PriorityQueue):

    def __init__(self):
        super(MergeablePriorityQueue, self).__init__()

    def merge(self, queue):
        pass
    merge = abstractmethod(merge)
