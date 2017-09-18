#
# This file contains the Python code from Program 5.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_12.txt
#
class Association(Object):

    def _compareTo(self, assoc):
        assert isinstance(self, assoc.__class__)
        return cmp(self.key, assoc.key)

    def __str__(self):
        return "Association %s" % str(self._tuple)

    # ...
