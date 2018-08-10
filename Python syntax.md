# 1. if...else...return
      def number_to_name(number):
          # It converts a number in the range 0 to 4 into its corresponding name as a string using if/elif/else.
          # Don't forget to return the result!

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
