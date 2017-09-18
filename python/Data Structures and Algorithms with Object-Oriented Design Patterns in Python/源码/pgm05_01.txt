#
# This file contains the Python code from Program 5.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_01.txt
#
class Object(object):

    def __init__(self):
        super(Object, self).__init__()

    def __cmp__(self, obj):
        if isinstance(self, obj.__class__):
            return self._compareTo(obj)
        elif isinstance(obj, self.__class__):
            return -obj._compareTo(self)
        else:
            return cmp(self.__class__.__name__,
                obj.__class__.__name__)

    def _compareTo(self, obj):
        pass
    _compareTo = abstractmethod(_compareTo)
    # ...
