#
# This file contains the Python code from Program 12.15 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_15.txt
#
class MultisetAsLinkedList(Multiset):

    def __and__(self, set):
	assert isinstance(set, MultisetAsLinkedList)
	assert self._universeSize == set._universeSize
        result = MultisetAsLinkedList(self._universeSize)
        p = self._list.head
        q = set._list.head
        while p is not None and q is not None:
            diff = p.datum - q.datum
            if diff == 0:
                result._list.append(p.datum)
            if diff <= 0:
                p = p.next
            if diff >= 0:
                q = q.next
        return result

    # ...
