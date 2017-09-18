#
# This file contains the Python code from Program 15.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm15_05.txt
#
class QuickSorter(Sorter):

    def __init__(self):
        super(QuickSorter, self).__init__()

    def selectPivot(self):
        pass
    selectPivot = abstractmethod(selectPivot)

    # ...
