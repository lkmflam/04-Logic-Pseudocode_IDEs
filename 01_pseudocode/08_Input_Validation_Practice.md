# Input Validation Exercise Workbench

Design an algorithm that prompts the user to enter a positive nonzero number and validates the input.

main()
   Declare int num
   Display "Please enter a positive number."
   Input num
   If num <= 0 then
      Display "That is not a valid number, please try again"
      Input num
    Else
      Display "Thank you for your input. The number that you logged is: ", num
   End If
   
Design an algorithm that prompts the user to enter a number in the range of 1 through 100 and validates the input.

main()
   Declare int num
   Display "Please enter a number between 1 and 100."
   Input num
      If 1 > num < 100 OR != integer then       <<< Look up how to say "If not an integer value"
         Display "You have entered an invalid value. You are the worst. Please try again... correctly."
         Input num
   Display num
   
Design an algorithm that prompts the user to enter “yes” or “no” and validates the input. (Use a case-insensitive comparison.)

main()
Declare string answer
Display "Do you think the news today intends to pit the country against itself? Please answer yes or no."
Input answer
   If answer != "yes" OR != "no"

Design an algorithm that prompts the user to enter a number that is greater than 99 and validates the input.

Design an algorithm that prompts the user to enter a secret word. The secret word should be at least 8 characters long. Validate the input.

# Debugging Exercises

Why does the following pseudocode not perform as indicated in the comments?
```
// This program asks the user to enter a value
// between 1 and 10 and validates the input.
Declare Integer value

// Get a value from the user.
Display "Enter a value between 1 and 10."
Input value

// Make sure the value is between 1 and 10.
While value < 1 AND value > 10           >>> Say if the value was 0, it wouldn't trigger on the > 10 so                                                  it would allow it to pass                 
   Display "ERROR: The value must be between 1 and 10."
   Display "Enter a value between 1 and 10."
   Input value
End While
```
Why does the following pseudocode not perform as indicated in the comments?
```
// This program gets a dollar amount from the user
// and validates the input.
Declare Real amount

// Get the amount from the user.
Display "Enter a dollar amount"
Input amount

// Make sure the amount is not less than zero. If it is,
// get a new amount from the user.
While amount < 0
   Display "ERROR: The dollar amount cannot be less than 0."
   Display "Enter a dollar amount."
                                    >>> Never re-asks the user for input so it gets stuck in the loop                                           since it cannot recheck
End While
```
The following pseudocode works, but it performs a case-sensitive validation of the user’s input. How could the algorithm be improved so the user does not have to pay attention to capitalization when entering a name?
```
// This program asks the user to enter a string
// and validates the input.
Declare String choice

// Get the user's response.
Display "Cast your vote for Chess Team Captain."
Display "Would you like to nominate Lisa or Tim?"
Input choice

// Validate the input.
While choice != "Lisa" AND choice != "Tim"
   Display "Please enter Lisa or Tim."
   Display "Cast your vote for Chess Team Captain."
   Display "Would you like to nominate Lisa or Tim?"
   Input response
End While
```
>>> Check against lower and upper and not specific string
