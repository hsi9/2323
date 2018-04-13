# 12th April

# Recurrence
  A recurrence relation is a set of equations that defines a function of one or more numbers recursively.
  
    f(n)=f(n−1)+1  →  f(n)=n
    f(n)=f(n−1)+n  →  f(n)=1/2n(n+1)
    f(n)=2f(n−1)   →  f(n)=2^n−1
    f(n)=nf(n−1)   →  f(n)=n!
    f(n)=f(n/2)+1  →  f(n)≈log2(n)+1
    f(n)=f(n/2)+n  →  f(n)≈2n−1
    f(n)=2f(n/2)   →  f(n)≈n
    f(n)=2f(n/2)+1 →  f(n)≈2n−1
    f(n)=2f(n/2)+n →  f(n)≈n(log2(n)+1)

# 1. Write a function slice(my_list, first, last) that takes as input a list my_list and two non-negative integer indices first and last satisfying 0≤first≤last≤n where n is the length of my_list. slice should return the corresponding Python list slice my_list[first:last]. For example, slice(['a', 'b', 'c', 'd', 'e'], 2, 4]) should return ['c', 'd'].Important: Your solution should not use Python's built-in slice operator : anywhere in its implementation. Instead use the method pop to remove one element from the input list during each recursive call.

    def slice(my_list, first, last):
        if my_list == []:
            return []
        else:
            first_elem = my_list.pop(0)
            if first > 0:  
                rest_sliced = slice(my_list, first - 1, last - 1)
                return rest_sliced
            elif last > 0:
                rest_sliced = slice(my_list, 0, last - 1)
                return [first_elem] + rest_sliced
            else:
                return []
