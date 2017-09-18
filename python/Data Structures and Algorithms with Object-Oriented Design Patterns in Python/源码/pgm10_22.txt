#
# This file contains the Python code from Program 10.22 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_22.txt
#
class Algorithms(object):

    def translate(dictionary, input, output):
        searchTree = AVLTree()
        for line in dictionary.readlines():
            words = line.split()
	    assert len(words) == 2
            searchTree.insert(Association(words[0], words[1]))
        for line in input.readlines():
            for word in line.split():
                assoc = searchTree.find(Association(word))
                if assoc is None:
                    output.write(word + " ")
                else:
                    output.write(assoc.value + " ")
            output.write("\n")
    translate = staticmethod(translate)
