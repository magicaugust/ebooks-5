#
# This file contains the Python code from Program 14.9 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_09.txt
#
def Fibonacci(n, k):
    if n < k - 1:
        return 0
    elif n == k - 1:
        return 1
    else:
        f = [0] * (n + 1)
        for i in xrange(k - 1):
            f[i] = 0
        f[k - 1] = 1
        for i in xrange(k, n + 1):
            sum = 0
            for j in xrange(k + 1):
                sum += f[i - j]
            f[i] = sum
        return f[n]
