#
# This file contains the Python code from Program 11.17 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm11_17.txt
#
class BinomialQueue(MergeablePriorityQueue):

    def merge(self, queue):
        oldList = self._treeList
        self._treeList = LinkedList()
        self._count = 0
        p = oldList.head
        q = queue._treeList.head
        carry = None
        i = 0
        while p is not None or q is not None \
                or carry is not None:
            a = None
            if p is not None:
                tree = p.datum
                if tree.degree == i:
                    a = tree
                    p = p.next
            b = None
            if q is not None:
                tree = q.datum
                if tree.degree == i:
                    b = tree
                    q = q.next
            (sum, carry) = BinomialQueue.fullAdder(a, b, carry)
            if sum is not None:
                self.addTree(sum)
            i += 1
        queue.purge()

    # ...
