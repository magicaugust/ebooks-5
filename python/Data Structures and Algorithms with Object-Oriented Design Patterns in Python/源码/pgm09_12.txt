#
# This file contains the Python code from Program 9.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_12.txt
#
class NaryTree(Tree):

    def __init__(self, *args):
        super(NaryTree, self).__init__()
        if len(args) == 1:
            self._degree = args[0]
            self._key = None
            self._subtree = None
        elif len(args) == 2:
            self._degree = args[0]
            self._key = args[1]
            self._subtree = Array(self._degree)
            for i in xrange(self._degree):
                self._subtree[i] = NaryTree(self._degree)

    def purge(self):
        self._key = None
        self._subtree = None

    # ...
