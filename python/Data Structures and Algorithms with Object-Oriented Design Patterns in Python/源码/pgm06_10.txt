#
# This file contains the Python code from Program 6.10 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm06_10.txt
#
class Algorithms(object):

    def calculator(input, output):
        stack = StackAsLinkedList()
        for line in input.readlines():
            for word in line.split():
                if word == "+":
                    arg2 = stack.pop()
                    arg1 = stack.pop()
                    stack.push(arg1 + arg2)
                elif word == "*":
                    arg2 = stack.pop()
                    arg1 = stack.pop()
                    stack.push (arg1 * arg2)
                elif word == "=":
                    arg = stack.pop()
                    output.write(str(arg) + "\n")
                else:
                    stack.push(int(word))
    calculator = staticmethod(calculator)
