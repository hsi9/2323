# 10th April

# 1. sorting list of strings: http://www.codeskulptor.org/#poc_string_sort.py
details:
排序：两次循环，第一次将所有同字母string分类，第二次合并成一个list。


    NUM_CHARS = 26
    CHARACTERS = [chr(ord("a") + char_num) for char_num in range(NUM_CHARS)] 

    def order_by_letter(string_list, letter_pos):
        """
        Takes a list of strings and order them alphabetically 
        using the letter at the specified position
        """
        buckets = [[] for dummy_idx in range(NUM_CHARS)]
        for string in string_list:
            char_index = ord(string[letter_pos]) - ord("a")
            buckets[char_index] += [string]
        
        answer = []
        for char_index in range(NUM_CHARS):
            answer += buckets[char_index]
        return answer

# 2. Working with Distance Fields： http://www.codeskulptor.org/#poc_distance_solution.py
details:
在2D Grids上寻找到已知grid最短距离的grid。
 
 
    def manhattan_distance(row0, col0, row1, col1):
        """
        Compute the Manhattan distance between the cells
        (row0, col0) and (row1, col1)
        """
        return abs(row0 - row1) + abs(col0 - col1)
        
    def create_distance_field(entity_list):
        """
        Create a Manhattan distance field that contains the minimum distance to 
        each entity (zombies or humans) in entity_list
        Each entity is represented as a grid position of the form (row, col) 
        """
        distance_field = [[ GRID_HEIGHT + GRID_WIDTH \
                           for dummy_col in range(GRID_WIDTH)] \
                             for dummy_row in range(GRID_HEIGHT)]
        
        for row in range(GRID_HEIGHT):
            for col in range(GRID_WIDTH):
                distance = min([manhattan_distance(entity[0], entity[1], row, col) \
                                for entity in entity_list])
                distance_field[row][col] = distance
        return distance_field
        
# 3. BFS use queue in search and DFS use stack in search.
     http://www.codeskulptor.org/#poc_queue.py
   
# 4. BFS pseudo code:

        while boundary is not empty:
            current_cell  ←  dequeue boundary
            for all neighbor_cell of current_cell:
                if neighbor_cell is not in visited:
                    add neighbor_cell to visited
                    enqueue neighbor_cell onto boundary
            
# 5. http://www.codeskulptor.org/#user44_HE3W5HDbet_16.py
    line129 - line147注意new_position要在for循环前define，这样才没有local variable无法引用的问题。
