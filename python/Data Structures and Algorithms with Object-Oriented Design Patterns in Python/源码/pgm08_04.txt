#
# This file contains the Python code from Program 8.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_04.txt
#
class Container(Object):

    def __hash__(self):
	result = hash(self.__class__)
	for obj in self:
	    result = (result + hash(obj)) & sys.maxint
	return result

    # ...
