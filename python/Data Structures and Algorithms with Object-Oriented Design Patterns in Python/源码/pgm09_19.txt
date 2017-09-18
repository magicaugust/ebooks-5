#
# This file contains the Python code from Program 9.19 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_19.txt
#
class ExpressionTree(BinaryTree):

    def __init__(self, word):
        super(ExpressionTree, self).__init__(word)
    
    def parsePostfix(input):
        stack = StackAsLinkedList()

        for line in input.readlines():
            for word in line.split():
                if word == "+" or word == "-" \
                        or word == "*" or word == "/":
                    result = ExpressionTree(word)
                    result.attachRight(stack.pop())
                    result.attachLeft(stack.pop())
                    stack.push(result)
                else:
                    stack.push(ExpressionTree(word))
        return stack.pop()
    parsePostfix = staticmethod(parsePostfix)

    # ...
