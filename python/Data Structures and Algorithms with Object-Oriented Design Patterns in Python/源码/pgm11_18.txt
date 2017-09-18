#
# This file contains the Python code from Program 11.18 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_18.txt
#
class BinomialQueue(MergeablePriorityQueue):

    def fullAdder(a, b, c):
	if a is None:
	    if b is None:
		if c is None:
		    return (None, None)
		else:
		    return (c, None)
	    else:
		if c is None:
		    return (b, None)
		else:
		    return (None, b.add(c))
	else:
	    if b is None:
		if c is None:
		    return (a, None)
		else:
		    return (None, a.add(c))
	    else:
		if c is None:
		    return (None, a.add(b))
		else:
		    return (c, a.add(b))
    fullAdder = staticmethod(fullAdder)

    # ...
