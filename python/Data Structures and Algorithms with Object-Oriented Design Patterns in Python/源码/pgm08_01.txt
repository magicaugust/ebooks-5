#
# This file contains the Python code from Program 8.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_01.txt
#
class Integer(int, Object):

    def __hash__(self):
	return self & sys.maxint

    # ...
