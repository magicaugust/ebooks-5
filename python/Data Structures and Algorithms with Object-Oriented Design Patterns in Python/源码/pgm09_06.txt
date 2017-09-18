#
# This file contains the Python code from Program 9.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_06.txt
#
class PostOrder(PrePostVisitor):

    def __init__(self, visitor):
        super(PostOrder, self).__init__()
        self._visitor = visitor

    def postVisit(self, obj):
        self._visitor.visit(obj)
    
    def getIsDone(self):
        return self._visitor.isDone
