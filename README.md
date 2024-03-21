# NAME: Linnea P. Castro
# CLASS: CSE 224
# DATE: 02 NOV 2022
# SYNOPSIS:

# This Bash script plays a number guessing game with a user.  The user guesses a number and the computer is uses an algorithm to guess, narrow down, 
# and ultimately select the exact number guessed.  The user gives feedback to the computer following each guess which allows the computer to 
# process the algorithm with a more refined number range and also ensures that only legitimate numbers reach the function.

# The default settings ask the user to think of a number between 1 and 100.  This script allows the user to customize the ceiling of numbers selected 
# with a command line argument, and then stores that as the $high value instead of default 100.  At the beginning of a game, a counter is
# initialized to 0 to keep track of total guesses.  I utilized one function in this script to run high and low values through an algorithm to
# select the computer's guess.  The function also increments the total guess counter. 

# I used two infinite loops in this script, the first to initialize gameplay.  The only ways out of this loop are for the computer to make a correct 
# guess or for the user to be called out for cheating - both instances will exit the game.  The start of the gameplay loop checks for suspicious
# play; if $high is less than low, the user has with or without intent, made a mistake giving feedback on the computer's guess. If $high > $low
# the script will call the guess function, read the user's feedback as they key in either c, h, or l, store this key in $hint and then process it
# in the checkinghint infinite loop.  If the user enters c, it means the computer's guess was correct.  The total number of guesses is printed 
# and the game exits.  If the user enters l, it means the computer's guess was low.  The new low value will be set to guess+1, the script will break
# from the checkinghint loop and head to the top of the gameplay loop.  The user entering h means the computer's guess was high and the new high
# value will be set to high-1.  Anything other than h, c, or l entry from the user will prompt the computer to ask again, sending that key entry
# to the top of the checkinghint loop for examination. 

# Skills practiced: infinite loops for gameplay, creating a function, incrementing guesses inside the function and initializing variable outside of 
# it, organizing and creating a bash script.   
