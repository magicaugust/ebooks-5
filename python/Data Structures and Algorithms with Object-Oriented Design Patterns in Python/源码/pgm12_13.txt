#
# This file contains the Python code from Program 12.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_13.txt
#
class MultisetAsLinkedList(Multiset):

    def __init__(self, n):
        super(MultisetAsLinkedList, self).__init__(n)
        self._list = LinkedList()

    # ...
