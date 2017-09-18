#
# This file contains the Python code from Program 12.20 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_20.txt
#
class PartitionAsForest(Partition):

    def join(self, s, t):
	assert s in self and s._parent is None and \
	    t in self and t._parent is None and s is not t
        t._parent = s
        self._count -= 1

    # ...
