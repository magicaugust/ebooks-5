#
# This file contains the Python code from Program A.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm0A_11.txt
#
class Circle(GraphicalObject):

    def __init__(self, center, radius):
        super(Circle, self).__init__(center)
        self._radius = radius

    def draw(self):
        # ...
