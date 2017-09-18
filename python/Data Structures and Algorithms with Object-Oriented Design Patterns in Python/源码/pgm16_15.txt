#
# This file contains the Python code from Program 16.15 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm16_15.txt
#
class Algorithms(object):

    class Entry(object):

        def __init__(self):
            self.known = False
            self.distance = sys.maxint
            self.predecessor = sys.maxint
