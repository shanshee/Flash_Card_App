# Flash_Card_App

This code implements a simple flashcard application for learning French words. It uses the Tkinter library for the graphical user interface.

![Screenshot 2024-05-05 174651](https://github.com/shanshee/Flash_Card_App/assets/135793255/d52b706d-97c9-4850-93eb-c40fccbe3682)

A try-except block is used to attempt reading a CSV file named 'data/words_to_learn.csv' using the pandas library. If the file is not found (FileNotFoundError),
it will read from another CSV file named 'data/french_words.csv'.

The function is_known() is called when the user indicates that they know the current word. 
It removes the word from the to_learn list, saves the updated list back to 'data/words_to_learn.csv', 
and proceeds to display the next card using next_card().

![Screenshot 2024-05-05 174717](https://github.com/shanshee/Flash_Card_App/assets/135793255/8ab10393-8036-43cf-8ae2-1137bdfe7321)

The function flip_card() is used to flip the current card and display the English translation.

The script sets up the Tkinter window and configures its appearance.

It loads image files for the front and back of the flashcard, as well as images for the "right" and "wrong" buttons.

The script creates a canvas widget to display the flashcard. The canvas is configured with the background color and positioned on the grid.

Two buttons are created for "right" and "wrong" answers, which allow the user to indicate if they know the word or not.

The next_card() function is called, which randomly selects a French word from the to_learn list 
and displays it on the flashcard. A timer is also set to flip the card after 3000 milliseconds (3 seconds).

![Screenshot 2024-05-05 174638](https://github.com/shanshee/Flash_Card_App/assets/135793255/956bfc5a-cd83-4a2a-9d58-8d93fea51723)

The is_known() function is called when the "right" button is clicked. It removes the current word from the to_learn list, 
saves the updated list to 'data/words_to_learn.csv', and then proceeds to display the next card using next_card().

The flip_card() function is called by the timer set in the window.after() method. It flips the current card and displays the English translation.

The program will save the words that the user still needs to learn to a CSV file, 
and the user can continue the learning process until they have learned all the words in the list.
