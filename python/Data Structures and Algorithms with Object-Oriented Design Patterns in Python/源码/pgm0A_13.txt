#
# This file contains the Python code from Program A.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm0A_13.txt
#
class Square(Rectangle):

    def __init__(self, center, width):
        super(Square, self).__init__(center, width, width)
