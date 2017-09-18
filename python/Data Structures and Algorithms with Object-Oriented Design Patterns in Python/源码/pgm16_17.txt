#
# This file contains the Python code from Program 16.17 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_17.txt
#
class Algorithms(object):

    def FloydsAlgorithm(g):
        n = g.numberOfVertices
        distance = DenseMatrix(n, n)
        for v in xrange(n):
            for w in xrange(n):
                distance[v, w] = sys.maxint
        for e in g.edges:
            distance[e.v0.number, e.v1.number] = e.weight
        for i in xrange(n):
            for v in xrange(n):
                for w in xrange(n):
                    if distance[v, i] != sys.maxint and \
                        distance[i, w] != sys.maxint:
                        d = distance[v, i] + distance[i, w]
                        if distance[v, w] > d:
                            distance[v, w] = d
        result = DigraphAsMatrix(n)
        for v in xrange(n):
            result.addVertex(v)
        for v in xrange(n):
            for w in xrange(n):
                if distance[v, w] != sys.maxint:
                    result.addEdge(v, w, distance[v, w])
        return result
    FloydsAlgorithm = staticmethod(FloydsAlgorithm)
