#
# This file contains the Python code from Program 7.22 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm07_22.txt
#
class Polynomial(Container):

    class DifferentiatingVisitor(Visitor):

        def __init__(self):
            super(Polynomial.DifferentiatingVisitor, self) \
                .__init__()

        def visit(self, term):
	    term.differentiate()

    def differentiate(self):
        self.accept(self.DifferentiatingVisitor())
        zeroTerm = self.find(self.Term(0, 0))
        if zeroTerm is not None:
            self.withdraw(zeroTerm)

    # ...
