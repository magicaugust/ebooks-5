#
# This file contains the Python code from Program A.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm0A_08.txt
#
class Parent(Person):

    def __init__(self, name, sex, children):
        super(Parent, self).__init__(name, sex)
        self._children = children

    def getChild(self, i):
        return self._children[i]

    def __str__(self):
        # ...
