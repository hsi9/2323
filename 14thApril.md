
# 1. Merge
 while内部每次更新list1 or list2到while循环。
    
    def merge(list1, list2):
    """
    Merge two sorted lists.
    Returns a new sorted list containing those elements that are in
    either list1 or list2.
    """   
    new_list = []
    while len(list1) > 0 and len(list2) > 0:       
    	if list1[0] < list2[0]:
            new_list.append(list1[0])
            list1.pop(0)
        else:
            new_list.append(list2[0])
            list2.pop(0)
            
    if len(list1) == 0:
        return new_list + list2
    elif len(list2) == 0:
        return new_list + list1
# 2. Recurrence
 (1) return list, 所以加[]
 
 (2) +1, 因为要添加letter到最后一位的下一位。
    
    
    def gen_all_strings(word):
        """
        Generate all strings that can be composed from the letters in word
        in any order.

        Returns a list of all strings that can be formed from the letters
        in word.

        This function should be recursive.
        """
   
        if word == '':
            return [''] --------------------------------------------------(1)        
        first = word[0]
        rest = word[1:]    
        temp_string =[]
        for string in gen_all_strings(rest):
            for idx in range(len(string)+1):---------------------------------------------(2)
                temp_string.append(string[:idx]+first+string[idx:]) 
        return gen_all_strings(rest) + temp_string

