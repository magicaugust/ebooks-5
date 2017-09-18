#
# This file contains the Python code from Program 16.20 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_20.txt
#
class Algorithms(object):

    class EarliestTimeVisitor(Visitor):

        def __init__(self, earliestTime):
            super(Algorithms.EarliestTimeVisitor,self).__init__()
            self._earliestTime = earliestTime

        def visit(self, w):
            t = self._earliestTime[0]
            for e in w.incidentEdges:
                t = max(t,
                    self._earliestTime[e.v0.number] + e.weight)
            self._earliestTime[w.number] = t
