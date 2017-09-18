#
# This file contains the Python code from Program 12.22 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_22.txt
#
class PartitionAsForestV2(PartitionAsForest):

    def join(self, s, t):
	assert s in self and s._parent is None and \
	    t in self and t._parent is None and s is not t
        if s._count > t._count:
            t._parent = s
            s._count += t._count
        else:
            s._parent = t
            t._count += s._count
        self._count -= 1

    # ...
