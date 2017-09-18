#
# This file contains the Python code from Program 6.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_07.txt
#
class StackAsLinkedList(Stack):

    def push(self, obj):
        self._list.prepend(obj)
        self._count += 1

    def pop(self):
        if self._count == 0:
            raise ContainerEmpty
        result = self._list.first
        self._list.extract(result)
        self._count -= 1
        return result

    def getTop(self):
        if self._count == 0:
            raise ContainerEmpty
        return self._list.first

    # ...
