#
# This file contains the Python code from Program 14.16 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_16.txt
#
class ExponentialRV(RandomVariable):

    def __init__(self, mu):
        self._mu = mu

    def getNext(self):
        return -self._mu * math.log(RandomNumberGenerator.next);
