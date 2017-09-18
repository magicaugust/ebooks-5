#
# This file contains the Python code from Program 12.14 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_14.txt
#
class MultisetAsLinkedList(Multiset):

    def __or__(self, set):
	assert isinstance(set, MultisetAsLinkedList)
	assert self._universeSize == set._universeSize
        result = MultisetAsLinkedList(self._universeSize)
        p = self._list.head
        q = set._list.head
        while p is not None and q is not None:
            if p.datum <= q.datum:
                result._list.append(p.datum)
                p = p.next
            else:
                result._list.append(q.datum)
                q = q.next
        while p is not None:
            result._list.append(p.datum)
            p = p.next
        while q is not None:
            result._list.append(q.datum)
            q = q.next
        return result

    # ...
