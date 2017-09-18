#
# This file contains the Python code from Program 9.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_13.txt
#
class NaryTree(Tree):

    def getIsEmpty(self):
        return self._key is None

    def getKey(self):
        if self.isEmpty:
            raise StateError
        return self._key

    def attachKey(self, obj):
        if not self.isEmpty:
            raise StateError
        self._key = obj
        self._subtree = Array(self._degree)
        for i in xrange(self._degree):
            self._subtree[i] = NaryTree(self._degree)

    def detachKey(self):
        if not isLeaf:
            raise StateError
        result = self._key
        self._key = None
        self._subtree = None
        return result

    # ...
