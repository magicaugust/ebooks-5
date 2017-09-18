#
# This file contains the Python code from Program 6.21 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_21.txt
#
class DequeAsLinkedList(QueueAsLinkedList, Deque):

    def getTail(self):
        if self._count == 0:
            raise ContainerEmpty
        return self._list.last

    def dequeueTail(self):
        if self._count == 0:
            raise ContainerEmpty
        result = self._list.last
        self._list.extract(result)
        self._count -= 1
        return result

    # ...
