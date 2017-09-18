#
# This file contains the Python code from Program 11.21 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_21.txt
#
class Simulation(object):

    class Event(Association):

        def __init__(self, type, time):
            super(Simulation.Event, self).__init__(time, type)
        
        time = property(
            fget = lambda self: self.getKey())

        type = property(
            fget = lambda self: self.getValue())

    # ...
