#
# This file contains the Python code from Program 8.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_11.txt
#
class ChainedScatterTable(HashTable):

    NULL = -1

    class Entry(object):

        def __init__(self, obj, next):
            super(ChainedScatterTable.Entry, self).__init__()
            self._obj = obj
            self._next = next

    # ...
