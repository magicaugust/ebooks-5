#
# This file contains the Python code from Program 8.21 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_21.txt
#
class Algorithms(object):

    class Counter(object):

        def __init__(self, value):
            super(Algorithms.Counter, self).__init__()
            self._value = value

        def __repr__(self):
            return str(self._value)

        def __iadd__(self, value):
            self._value += value

    def wordCounter(input, output):
        table = ChainedHashTable(1031)
        for line in input.readlines():
            for word in line.split():
                assoc = table.find(Association(word))
                if assoc is None:
                    table.insert(Association(
                        word, Algorithms.Counter(1)))
                else:
                    counter = assoc.value
		    counter += 1
        output.write(str(table) + "\n")
    wordCounter = staticmethod(wordCounter)
