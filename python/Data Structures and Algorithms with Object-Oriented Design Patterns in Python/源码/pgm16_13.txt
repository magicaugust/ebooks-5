#
# This file contains the Python code from Program 16.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_13.txt
#
class Digraph(Graph):

    def getIsStronglyConnected(self):
        for v in xrange(self.numberOfVertices):
            visitor = self.CountingVisitor()
            self.depthFirstTraversal(PreOrder(visitor), v)
            if visitor.count != self.numberOfVertices:
                return False
        return True

    # ...
