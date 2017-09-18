#
# This file contains the Python code from Program A.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm0A_01.txt
#
def one():
    x = 1
    print x
    two(x)
    print x

def two(y):
    print y
    y = 2
    print y
