#
# This file contains the Python code from Program 8.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_03.txt
#
class String(str, Object):

    shift = 6

    mask = ~0 << (31 - shift)

    def __hash__(self):
        result = 0
        for c in self:
            result = ((result & String.mask) ^
		result << String.shift ^ ord(c)) & sys.maxint
        return result

    # ...
