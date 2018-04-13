# 12th April

# 1.Recurrence
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

# 2. Write a function slice(my_list, first, last) that takes as input a list my_list and two non-negative integer indices first and last satisfying 0≤first≤last≤n where n is the length of my_list. slice should return the corresponding Python list slice my_list[first:last]. For example, slice(['a', 'b', 'c', 'd', 'e'], 2, 4]) should return ['c', 'd'].Important: Your solution should not use Python's built-in slice operator : anywhere in its implementation. Instead use the method pop to remove one element from the input list during each recursive call.

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
# 3. Write a function remove_x(my_string) that takes the string my_string and deletes all occurrences of the character 'x' from this string. For example, remove_x("catxxdogx") should return "catdog". You should not use Python's built-in string methods.

    def remove_x(my_string):
        if my_string == "":
            return ""
        else:
            first_character = my_string[0]
            rest_removed = remove_x(my_string[1 :])
            if first_character == 'x':
                return rest_removed
            else:
                return first_character + rest_removed
   
# 4. Write a function insert_x(my_string) that takes the string my_string and adds the character 'x' between each pair of consecutive characters in the string. For example, insert_x("catdog") should return "cxaxtxdxoxg"

    def insert_x(my_string):  
        if len(my_string) <= 1:
            return my_string
        else:
            first_character = my_string[0]
            rest_inserted = insert_x(my_string[1 :])
            return first_character + 'x' + rest_inserted
