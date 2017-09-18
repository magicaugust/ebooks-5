#
# This file contains the Python code from Program 5.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_08.txt
#
class Container(Object):

    class StrVisitor(Visitor):

        def __init__(self):
            self._string = ""
            self._comma = False

        def visit(self, object):
            if self._comma:
                self._string = self._string + ", "
            self._string = self._string + str(object)
            self._comma = True

        def __str__(self):
            return self._string

    def __str__(self):
        visitor = Container.StrVisitor()
        self.accept(visitor)
        return "%s {%s}" % (self.__class__.__name__,str(visitor))

    # ...
