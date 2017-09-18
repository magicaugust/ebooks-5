#
# This file contains the Python code from Program 6.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_04.txt
#
class StackAsArray(Stack):

    def accept(self, visitor):
        assert isinstance(visitor, Visitor)
        for i in xrange(self._count):
            visitor.visit(self._array[i])
            if visitor.isDone:
                return

    #...
