#
# This file contains the Python code from Program 14.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_11.txt
#
def typeset(l, D, s):
    n = len(l)
    L = DenseMatrix(n, n)
    for i in xrange(n):
        L[i, i] = l[i]
        for j in xrange(i + 1, n):
            L[i, j] = L[i, j - 1] + l[j]
    P = DenseMatrix(n, n)
    for i in xrange(n):
        for j in xrange(i, n):
            if L[i, j] < D:
                P[i, j] = abs(D - L[i, j] - (j - i) * s)
            else:
                P[i, j] = sys.maxint
    c = DenseMatrix(n, n)
    for j in xrange(n):
        c[j, j] = P[j, j]
        i = j - 1
        while i >= 0:
            min = P[i, j]
            for k in xrange(i, j):
                tmp = P[i, k] + c[k + 1, j]
                if tmp < min:
                    min = tmp
            c[i, j] = min
            i -= 1
