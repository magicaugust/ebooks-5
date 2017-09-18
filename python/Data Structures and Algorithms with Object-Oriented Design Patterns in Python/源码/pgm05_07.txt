#
# This file contains the Python code from Program 5.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_07.txt
#
class Container(Object):

    def accept(self, visitor):
        assert isinstance(visitor, Visitor)
        for obj in self:
            visitor.visit(obj)

    # ...
