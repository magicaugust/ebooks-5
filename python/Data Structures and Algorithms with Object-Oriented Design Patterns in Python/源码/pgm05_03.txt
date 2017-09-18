#
# This file contains the Python code from Program 5.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_03.txt
#
class Container(Object):

    def __init__(self):
        super(Container, self).__init__()
        self._count = 0

    def purge(self):
        pass
    purge = abstractmethod(purge)

    def __iter__(self):
        pass
    __iter__ = abstractmethod(__iter__)

    # ...
