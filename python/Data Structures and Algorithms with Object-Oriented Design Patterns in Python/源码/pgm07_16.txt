#
# This file contains the Python code from Program 7.16 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_16.txt
#
class OrderedListAsLinkedList(OrderedList):

    def findPosition(self, obj):
        ptr = self._linkedList.head
        while ptr is not None:
            if ptr.datum == obj:
                break
            ptr = ptr.next
        return self.Cursor(self, ptr)

    # ...
