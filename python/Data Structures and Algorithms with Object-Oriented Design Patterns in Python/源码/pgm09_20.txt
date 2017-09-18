#
# This file contains the Python code from Program 9.20 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_20.txt
#
class ExpressionTree(BinaryTree):

    class InfixVisitor(PrePostVisitor):

        def __init__(self):
            self._s = ""

        def preVisit(self, obj):
            self._s = self._s + "("

        def inVisit(self, obj):
            self._s = self._s + str(obj)

        def postVisit(self, obj):
            self._s = self._s + ")"

        def __str__(self):
            return self._s

    def __str__(self):
        visitor = self.InfixVisitor()
        self.depthFirstTraversal(visitor)
        return str(visitor)

    # ...
