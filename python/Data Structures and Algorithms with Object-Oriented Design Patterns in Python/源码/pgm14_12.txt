#
# This file contains the Python code from Program 14.12 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_12.txt
#
class RandomNumberGenerator(object):

    a = 16807
    m = 2147483647
    q = 127773
    r = 2836

    def __init__(self, seed=1):
        super(RandomNumberGenerator, self).__init__()
	assert seed >= 1 and seed < self.m
        self._seed = seed

    def getSeed(self):
        return self._seed

    def setSeed(self, seed):
	assert seed >= 1 and seed < self.m
        self._seed = seed

    seed = property(
        fget = lambda self: self.getSeed(),
        fset = lambda self, value: self.setSeed(value))

    def getNext(self):
        self._seed = self.a * (self._seed % self.q) \
                - self.r * (self._seed / self.q)
        if self._seed < 0:
            self._seed += self.m
        return (1.0 * self._seed)  / self.m

    next = property(
        fget = lambda self: self.getNext())

RandomNumberGenerator = RandomNumberGenerator() # singleton
