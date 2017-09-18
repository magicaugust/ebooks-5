#
# This file contains the Python code from Program 6.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_09.txt
#
class StackAsLinkedList(Stack):

    class Iterator(Iterator):

        def __init__(self, stack):
            super(StackAsLinkedList.Iterator, self).__init__(
		stack)
            self._position = stack._list.head

        def next(self):
            if self._position is None:
		raise StopIteration
	    element = self._position
	    self._position = self._position.next
            return element.datum

    def __iter__(self):
        return self.Iterator(self)

    # ...
