#
# This file contains the Python code from Program 6.20 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_20.txt
#
class DequeAsLinkedList(QueueAsLinkedList, Deque):

    def __init__(self):
        super(DequeAsLinkedList, self).__init__()

    def enqueueHead(self, obj):
        self._list.prepend(obj);
        self._count += 1

    # ...
