#
# This file contains the Python code from Program 9.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_10.txt
#
class GeneralTree(Tree):

    def __init__(self, key):
        super(GeneralTree, self).__init__()
        self._key = key
        self._degree = 0
        self._list = LinkedList()

    def purge(self):
        self._list.purge()
        self._degree = 0
    # ...
