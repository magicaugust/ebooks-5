#
# This file contains the Python code from Program 11.14 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_14.txt
#
class BinomialQueue(MergeablePriorityQueue):

    def __init__(self, *args):
        super(BinomialQueue, self).__init__()
        self._treeList = LinkedList()
	if len(args) == 0:
	    pass
	elif len(args) == 1:
	    assert isinstance(args[0], self.BinomialTree)
	    self._treeList.append(args[0])
	else:
	    raise ValueError

    # ...
