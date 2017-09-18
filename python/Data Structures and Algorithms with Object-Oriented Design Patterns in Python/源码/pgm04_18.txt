#
# This file contains the Python code from Program 4.18 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm04_18.txt
#
class LinkedList(object):

    def __copy__(self):
        result = LinkedList()
        ptr = list._head
        while ptr is not None:
            result.append(ptr._datum)
            ptr = ptr._next
        return result

    # ...
