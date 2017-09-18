#
# This file contains the Python code from Program 7.30 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_30.txt
#
class SortedListAsLinkedList(
    OrderedListAsLinkedList, SortedList):

    def insert(self, obj):
        prevPtr = None
        ptr = self._linkedList.head
        while ptr is not None:
            if ptr.datum >= obj:
                break
            prevPtr = ptr
            ptr = ptr.next
        if prevPtr is None:
            self._linkedList.prepend(obj)
        else:
            prevPtr.insertAfter(obj)
        self._count += 1

    # ...
