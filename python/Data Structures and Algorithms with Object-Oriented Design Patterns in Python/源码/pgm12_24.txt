#
# This file contains the Python code from Program 12.24 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm12_24.txt
#
class Algorithms(object):

    def equivalenceClasses(input, output):
        line = input.readline()
        p = PartitionAsForest(int(line))
        for line in input.readlines():
            words = line.split()
            i = int(words[0])
            j = int(words[1])
            s = p.find(i)
            t = p.find(j)
            if s is not t:
                p.join(s, t)
            else:
                output.write("redundant pair: %d, %d\n" % (i, j))
        output.write(str(p) + "\n")
    equivalenceClasses = staticmethod(equivalenceClasses)
