# 1. if...else...return
      def number_to_name(number):
          if number == 0:
              nam = "rock"
          elif number == 1:
              nam = "Spock"
          elif number == 2:
              nam = "paper"
          elif number == 3:
              nam = "lizard"
          elif number == 4:
              nam = "scissors"
          else:
              print "Number out of range."
          return nam
# 2. You dont need to say global if you are just using a global variable, you only need to say this when you are updating a global variable.
# 3. To measure how fast to click the mouse twice.
      total_ticks = 0
      first_click = True

      # Timer handler
      def tick():
            global total_ticks
            total_ticks += 1
    
      # Button handler
      def click():
            global total_ticks, first_click
            if first_click:
                  first_click = False
                  total_ticks = 0
                  timer.start()
            else:
                  first_click = True
                  timer.stop()
                  print "Time between clicks is " + str(total_ticks / 100.0) + " seconds"
                  total_ticks = 0
# 4. Format time in A:BC:D
      def format(t):
            A = t // 600
            B = t % 600 //100
            C = t % 100 //10  
            D = t % 10
            return str(A) + ":" + str(B) + str(C) + "." + str(D)
            
# 5. If reference issue is confused, you can use list to make a copy of things, so you can modify it but not the other.
# 6. Remove the last odd number from a list
      def remove_last_odd(numbers):
            has_odd = False
            last_odd = 0
            for num in numbers:
                  if num % 2 == 1:
                        has_odd = True
                        last_odd = num
            
            if has_odd:
                  numbers.remove(last_odd)
# 7. String List Joining
      def string_list_join(string_list):
            ans = ""
            for i in range(len(string_list)):
                  ans += string_list[i]
            return ans
# 8. [x for x in range(8)]*2
# 9. status change
      def status():
            global state
            if state == 0:
                  state = 1
            elif state == 1:
                  state = 2
            else:
                  state = 1
# 10. Class -- def __init__()
      class xxxx:
            def __init__(self, A,B):
                  self.A = A  (left A is field name, right A is argument value assigned to the filed)
                  self.X = B  (x is field name, B is value assigned)
      A and B can be an output by calling another class, list, etc.

# 11. random choose items from a list without replacement, should use shuffle() the list first then use pop().

# 12. Return the index of a position of a list by some conditions that is closest to the 0 position:
            for A in range(1, len(list)):
                  if condition:
                        return A
# 13. The running time of BFS can be O(n^2) when a graph is dense or O(m+n) when a graph is loose.
# week 5a - List Examples, 5b - Dictionaries - create random dictionary,
