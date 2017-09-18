#
# This file contains the Python code from Program 9.17 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_17.txt
#
class BinaryTree(Tree):

    def depthFirstTraversal(self, visitor):
        assert isinstance(visitor, PrePostVisitor)
        if not self.isEmpty:
            visitor.preVisit(self.key)
            self.left.depthFirstTraversal(visitor)
            visitor.inVisit(self.key)
            self.right.depthFirstTraversal(visitor)
            visitor.postVisit(self.key)

    # ...
