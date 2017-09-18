#
# This file contains the Python code from Program 4.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_13.txt
#
class LinkedList(object):

    def purge(self):
        self._head = None
        self._tail = None

    # ...
