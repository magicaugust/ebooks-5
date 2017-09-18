#
# This file contains the Python code from Program A.7 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm0A_07.txt
#
class Person(object):

    FEMALE = 0
    MALE = 1

    def __init__(self, name, sex):
        super(Person, self).__init__()
        self._name = name
        self._sex = sex

    def __str__(self):
        return str(self._name)
