#
# This file contains the Python code from Program 14.17 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_17.txt
#
def pi(trials):
    hits = 0
    for i in xrange(trials):
        x = RandomNumberGenerator.next
        y = RandomNumberGenerator.next
        if x * x + y * y < 1.0:
            hits += 1
    return 4.0 * hits / trials
