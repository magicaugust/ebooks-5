#
# This file contains the Python code from Program 8.6 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm08_06.txt
#
class HashTable(SearchableContainer):

    def __init__(self):
        super(HashTable, self).__init__()

    def __len__(self):
        pass
    __len__ = abstractmethod(__len__)

    def getLoadFactor(self):
        return self.count / len(self)

    loadFactor = property(
        fget = lambda self: self.getLoadFactor())

    # ...
