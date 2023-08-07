# Flash_Card_App

This code implements a simple flashcard application for learning French words. It uses the Tkinter library for the graphical user interface.

A try-except block is used to attempt reading a CSV file named 'data/words_to_learn.csv' using the pandas library. If the file is not found (FileNotFoundError),
it will read from another CSV file named 'data/french_words.csv'.

The function is_known() is called when the user indicates that they know the current word. 
It removes the word from the to_learn list, saves the updated list back to 'data/words_to_learn.csv', 
and proceeds to display the next card using next_card().

The function flip_card() is used to flip the current card and display the English translation.

The script sets up the Tkinter window and configures its appearance.

It loads image files for the front and back of the flashcard, as well as images for the "right" and "wrong" buttons.

The script creates a canvas widget to display the flashcard. The canvas is configured with the background color and positioned on the grid.

Two buttons are created for "right" and "wrong" answers, which allow the user to indicate if they know the word or not.

The next_card() function is called, which randomly selects a French word from the to_learn list 
and displays it on the flashcard. A timer is also set to flip the card after 3000 milliseconds (3 seconds).

The is_known() function is called when the "right" button is clicked. It removes the current word from the to_learn list, 
saves the updated list to 'data/words_to_learn.csv', and then proceeds to display the next card using next_card().

The flip_card() function is called by the timer set in the window.after() method. It flips the current card and displays the English translation.

The program will save the words that the user still needs to learn to a CSV file, 
and the user can continue the learning process until they have learned all the words in the list.
