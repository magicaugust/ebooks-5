#
# This file contains the Python code from Program 16.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_11.txt
#
class Digraph(Graph):

    def topologicalOrderTraversal(self, visitor):
        inDegree = Array(self.numberOfVertices)
        for v in xrange(self.numberOfVertices):
            inDegree[v] = 0
        for e in self.edges:
            inDegree[e.v1.number] += 1
        queue = QueueAsLinkedList()
        for v in xrange(self.numberOfVertices):
            if inDegree[v] == 0:
                queue.enqueue(self[v])
        while not queue.isEmpty and not visitor.isDone:
            v = queue.dequeue()
            visitor.visit(v)
            for to in v.successors:
                inDegree[to.number] -= 1
                if inDegree[to.number] == 0:
                    queue.enqueue(to)

    # ...
