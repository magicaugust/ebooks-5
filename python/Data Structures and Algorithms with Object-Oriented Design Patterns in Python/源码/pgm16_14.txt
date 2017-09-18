#
# This file contains the Python code from Program 16.14 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_14.txt
#
class Digraph(Graph):

    def getIsCyclic(self):
        visitor = self.CountingVisitor()
        self.topologicalOrderTraversal(visitor)
        return visitor.count != self.numberOfVertices

    # ...
