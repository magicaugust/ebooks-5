#
# This file contains the Python code from Program 16.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_09.txt
#
class Graph(Container):

    def depthFirstTraversal(self, visitor, start):
        assert isinstance(visitor, PrePostVisitor)
        visited = Array(self._numberOfVertices)
        for v in xrange(self._numberOfVertices):
            visited[v] = False
        self._depthFirstTraversal(visitor, self[start], visited)

    def _depthFirstTraversal(self, visitor, v, visited):
        if visitor.isDone:
            return
        visitor.preVisit(v)
        visited[v.number] = True
        for to in v.successors:
            if not visited[to.number]:
                self._depthFirstTraversal(visitor, to, visited)
        visitor.postVisit(v)

    # ...
