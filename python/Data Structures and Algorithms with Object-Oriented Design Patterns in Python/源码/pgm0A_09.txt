#
# This file contains the Python code from Program A.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm0A_09.txt
#
class GraphicalObject(Object):

    def __init__(self, center):
        super(GraphicalObject, self).__init__()
        self._center = center

    def draw(self):
        pass
    draw = abstractmethod(draw)

    def erase(self):
        self.setPenColor(self.BACKGROUND_COLOR)
        self.draw()
        self.setPenColor(self.FOREGROUND_COLOR)

    def moveTo(self, p):
        self.erase()
        self._center = p
        self.draw()
