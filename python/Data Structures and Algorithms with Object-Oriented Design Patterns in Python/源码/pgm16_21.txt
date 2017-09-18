#
# This file contains the Python code from Program 16.21 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_21.txt
#
class Algorithms(object):

    def criticalPathAnalysis(g):
        n = g.numberOfVertices

        earliestTime = Array(n)
        earliestTime[0] = 0
        g.topologicalOrderTraversal(
            Algorithms.EarliestTimeVisitor(earliestTime))

        latestTime = Array(n)
        latestTime[n - 1] = earliestTime[n - 1]
        g.depthFirstTraversal(PostOrder(
            Algorithms.LatestTimeVisitor(latestTime)), 0)

        slackGraph = DigraphAsLists(n)
        for v in xrange(n):
            slackGraph.addVertex(v)
        for e in g.edges:
            slack = latestTime[e.v1.number] - \
                earliestTime[e.v0.number] - e.weight
            slackGraph.addEdge(
                e.v0.number, e.v1.number, e.weight)
        return Algorithms.DijkstrasAlgorithm(slackGraph, 0)
    criticalPathAnalysis = staticmethod(criticalPathAnalysis)
