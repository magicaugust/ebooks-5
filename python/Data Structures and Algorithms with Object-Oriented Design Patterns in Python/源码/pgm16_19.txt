#
# This file contains the Python code from Program 16.19 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_19.txt
#
class Algorithms(object):

    def KruskalsAlgorithm(g):
        n = g.numberOfVertices
        result = GraphAsLists(n)
        for v in xrange(n):
            result.addVertex(v)
        queue = BinaryHeap(g.numberOfEdges)
        for e in g.edges:
            weight = e.weight
            queue.enqueue(Association(weight, e))
        partition = PartitionAsForest(n)
        while not queue.isEmpty and partition.count > 1:
            assoc = queue.dequeueMin()
            e = assoc.value
            n0 = e.v0.number
            n1 = e.v1.number
            s = partition.find(n0)
            t = partition.find(n1)
            if s != t:
                partition.join(s, t)
                result.addEdge(n0, n1)
        return result
    KruskalsAlgorithm = staticmethod(KruskalsAlgorithm)
