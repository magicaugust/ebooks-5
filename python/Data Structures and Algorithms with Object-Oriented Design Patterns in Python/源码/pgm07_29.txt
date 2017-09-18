#
# This file contains the Python code from Program 7.29 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_29.txt
#
class SortedListAsLinkedList(
    OrderedListAsLinkedList, SortedList):

    def __init__(self):
        super(SortedListAsLinkedList, self).__init__()

    # ...
