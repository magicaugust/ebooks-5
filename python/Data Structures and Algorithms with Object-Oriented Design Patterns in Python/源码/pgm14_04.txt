#
# This file contains the Python code from Program 14.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_04.txt
#
class BreadthFirstSolver(Solver):

    def __init__(self):
        super(BreadthFirstSolver, self).__init__()

    def search(self, initial):
        queue = QueueAsLinkedList()
        queue.enqueue(initial)
        while not queue.isEmpty:
            current = queue.dequeue()
            if current.isComplete:
                self.updateBest(current)
            else:
                for soln in current.successors:
                    queue.enqueue(soln)
