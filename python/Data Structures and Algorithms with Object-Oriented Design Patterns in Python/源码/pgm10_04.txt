#
# This file contains the Python code from Program 10.4 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_04.txt
#
class BinarySearchTree(BinaryTree, SearchTree):

    def insert(self, obj):
        if self.isEmpty:
            self.attachKey(obj)
        else:
            diff = cmp(obj, self._key)
            if diff == 0:
                raise ValueError
            elif diff < 0:
                self._left.insert(obj)
            elif diff > 0:
                self._right.insert(obj)
        self.balance()

    def attachKey(self, obj):
        if not self.isEmpty:
            raise StateError
        self._key = obj
        self._left = BinarySearchTree()
        self._right = BinarySearchTree()

    def balance(self):
        pass

    # ...
