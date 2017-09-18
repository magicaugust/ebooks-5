#
# This file contains the Python code from Program 7.15 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_15.txt
#
class OrderedListAsLinkedList(OrderedList):

    class Cursor(Cursor):

        def __init__(self, list, element):
	    super(OrderedListAsLinkedList.Cursor, self) \
		.__init__(list)
            self._element = element

        def getDatum(self):
            return self._element.datum

        # ...

    # ...
