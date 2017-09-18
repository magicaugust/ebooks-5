#
# This file contains the Python code from Program 12.23 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_23.txt
#
class PartitionAsForestV3(PartitionAsForestV2):

    def join(self, s, t):
	assert s in self and s._parent is None and \
	    t in self and t._parent is None and s is not t
        if s._rank > t._rank:
            t._parent = s
        else:
            s._parent = t
            if s._rank == t._rank:
                t._rank += 1
        self._count -= 1

    # ...
