#
# This file contains the Python code from Program A.14 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm0A_14.txt
#
class A(Exception):
    pass

def f():
    raise A

def g():
    try:
        f()
    except A:
        # ...
