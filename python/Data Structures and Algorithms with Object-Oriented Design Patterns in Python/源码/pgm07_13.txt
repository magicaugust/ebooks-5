#
# This file contains the Python code from Program 7.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_13.txt
#
class OrderedListAsLinkedList(OrderedList):

    def __contains__(self, obj):
        ptr = self._linkedList.head
        while ptr is not None:
            if ptr.datum is obj:
                return True
            ptr = ptr.next
        return False

    def find(self, arg):
        ptr = self._linkedList.head
        while ptr is not None:
            obj = ptr.datum
            if obj == arg:
                return obj
            ptr = ptr.next
        return None

    # ...
