#
# This file contains the Python code from Program 16.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_12.txt
#
class Graph(Container):

    class CountingVisitor(Visitor):

        def __init__(self):
            super(Graph.CountingVisitor, self).__init__()
            self._count = 0

        def visit(self, obj):
            self._count += 1
        
        def getCount(self):
            return self._count

        count = property(
            fget = lambda self: self.getCount())

    def getIsConnected(self):
        visitor = self.CountingVisitor()
        self.depthFirstTraversal(PreOrder(visitor), 0)
        return visitor.count == self.numberOfVertices

    # ...
