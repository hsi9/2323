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
