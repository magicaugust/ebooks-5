#
# This file contains the Python code from Program 10.14 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_14.txt
#
class MWayTree(SearchTree):

    def depthFirstTraversal(self, visitor):
        assert isinstance(visitor, PrePostVisitor)
        if not self.isEmpty:
            for i in xrange(self._count + 2):
                if i > 1:
                    visitor.postVisit(self._key[i - 1])
                if i >= 1 and i <= self._count:
                    visitor.inVisit(self._key[i])
                if i < self._count:
                    visitor.preVisit(self._key[i + 1])
                if i <= self._count:
                    self._subtree[i].depthFirstTraversal(visitor)

    # ...
