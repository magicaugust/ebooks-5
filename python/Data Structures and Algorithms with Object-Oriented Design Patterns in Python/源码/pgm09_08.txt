#
# This file contains the Python code from Program 9.8 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_08.txt
#
class Tree(Container):

    def accept(self, visitor):
        assert isinstance(visitor, Visitor)
        self.depthFirstTraversal(PreOrder(visitor))

    # ...
