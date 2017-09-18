#
# This file contains the Python code from Program A.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm0A_12.txt
#
class Rectangle(GraphicalObject):

    def __init__(self, center, height, width):
        super(Rectangle, self).__init__(center)
        self._height = height
        self._width = width

    def draw(self):
        # ...
