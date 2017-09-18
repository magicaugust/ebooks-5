#
# This file contains the Python code from Program 5.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_10.txt
#
class Association(Object):

    def __init__(self, *args):
        if len(args) == 1:
            self._tuple = (args[0], None)
        elif len(args) == 2:
            self._tuple = args
        else:
            raise ValueError

    # ...
