#
# This file contains the Python code from Program 8.15 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_15.txt
#
class OpenScatterTable(HashTable):

    EMPTY = 0
    OCCUPIED = 1
    DELETED = 2

    class Entry(object):

        def __init__(self, state, obj):
            super(OpenScatterTable.Entry, self).__init__()
            self._state = state
            self._obj = obj

    # ...
