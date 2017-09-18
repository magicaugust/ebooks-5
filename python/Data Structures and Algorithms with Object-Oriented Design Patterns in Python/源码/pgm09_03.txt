#
# This file contains the Python code from Program 9.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_03.txt
#
class PrePostVisitor(Visitor):

    def __init__(self):
        super(PrePostVisitor, self).__init__()

    def preVisit(self, obj):
        pass

    def inVisit(self, obj):
        pass

    def postVisit(self, obj):
        pass

    visit = inVisit
