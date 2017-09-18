#
# This file contains the Python code from Program 16.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_03.txt
#
class Graph(Container):

    def __init__(self, size):
        super(Graph, self).__init__()
        self._numberOfVertices = 0
        self._numberOfEdges = 0
        self._vertex = Array(size)
        self._isDirected = False

    class Vertex(Vertex):

        def __init__(self, graph, number, weight):
            super(Graph.Vertex, self).__init__()
            self._graph = graph
            self._number = number
            self._weight = weight

        # ...

    class Edge(Edge):

        def __init__(self, graph, v0, v1, weight):
            super(Graph.Edge, self).__init__()
            self._graph = graph
            self._v0 = v0
            self._v1 = v1
            self._weight = weight

        # ...

    # ...
