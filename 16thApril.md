
# 1. 两段求intersection和merge非常相似。

    def intersect(list1, list2):
    """
    Compute the intersection of two sorted lists.

    Returns a new sorted list containing only elements that are in
    both list1 and list2.

    This function can be iterative.
    """
    new_list = []
    idx1 = 0
    idx2 = 0
    while idx1 < len(list1) and idx2 < len(list2):
        if list1[idx1] < list2[idx2]:
            idx1 += 1
        elif list1[idx1] > list2[idx2]:
            idx2 += 1
        else:
            new_list.append(list1[idx1])
            idx1 += 1
            idx2 += 1
            
    return new_list
    #return [value for value in list1 if value in list2]

    Functions to perform merge sort

    def merge(list1, list2):
    """
    Merge two sorted lists.

    Returns a new sorted list containing those elements that are in
    either list1 or list2.

    This function can be iterative.
    """   
    new_list = []
    new_list1 = list(list1)
    new_list2 = list(list2)
    while len(new_list1) > 0 and len(new_list2) > 0:       
        if new_list1[0] < new_list2[0]:
            new_list.append(new_list1[0])
            new_list1.pop(0)
        else:
            new_list.append(new_list2[0])
            new_list2.pop(0)
                   
    if len(new_list1) == 0:
        return new_list + new_list2
    elif len(new_list2) == 0:
        return new_list + new_list1 
