#
# This file contains the Python code from Program 6.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_06.txt
#
class StackAsLinkedList(Stack):

    def __init__(self):
        super(StackAsLinkedList, self).__init__()
        self._list = LinkedList()

    def purge(self):
        self._list.purge()
        self._count = 0

    # ...
