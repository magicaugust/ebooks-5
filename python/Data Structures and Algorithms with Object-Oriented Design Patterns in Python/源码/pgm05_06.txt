#
# This file contains the Python code from Program 5.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm05_06.txt
#
class Visitor(Object):

    def __init__(self):
        super(Visitor, self).__init__()

    def visit(self, obj):
        pass
    
    def getIsDone(self):
        return False

    isDone = property(
        fget = lambda self: self.getIsDone())
