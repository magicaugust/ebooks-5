#
# This file contains the Python code from Program 5.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_05.txt
#
class Iterator(Object):

    def __init__(self, container):
        super(Object, self).__init__()
        self._container = container

    def __iter__(self):
        return self

    def next(self):
        pass
    next = abstractmethod(next)

    # ...
