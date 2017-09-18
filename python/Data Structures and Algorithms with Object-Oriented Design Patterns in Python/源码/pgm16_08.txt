#
# This file contains the Python code from Program 16.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_08.txt
#
class GraphAsLists(Graph):
    "Graph implemented using adjacency lists."

    def __init__(self, size):
        super(GraphAsLists, self).__init__(size)
        self._adjacencyList = Array(size)
        for i in xrange(size):
            self._adjacencyList[i] = LinkedList()

    # ...
