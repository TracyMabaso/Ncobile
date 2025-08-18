Perceptron Lab Exercise1 answers:


Q1: What does the prediction -1 mean for the book [size=3, color=2]?
The guess of -1 means the Perceptron thinks the book is non-fiction(real stories). In this group of data, +1 means fiction (made-up stories), and -1 means non-fiction. So, the computer thinks the book with size 3 and color 2 is a non-fiction book.


Q2: How many total errors did the Perceptron make across all 10 epochs?
The Perceptron made 8 mistakes during the 10 rounds of learning. We count the mistakes like this 
2 + 1 + 2 + 1 + 1 + 1 + 0 + 0 + 0 + 0 = 8
Each mistake means the computer had to change its rules because it guessed wrong

Q3: Why do the errors drop to 0 by epoch 7? What does this tell you about the dataset 
The mistakes stop at 0 by round 7 because the Perceptron has learned the right way to tell the difference between fiction and non-fiction books. When it stops guessing wrong, it doesn’t need to change its rules anymore.  
This shows that the data is easy to split a straight line can separate the two types of books based on their size and color.


 Conclusion  
In this lab, the Perceptron acted like a robot helper in a library. It learned how to tell apart fiction and non-fiction books by changing its rules each time it made a mistake. At first, it got things wrong, but after some practice, it got better and made no mistakes after round 7.  
This means the data is simple and can be split clearly, so the Perceptron can sort the books correctly using a straight line.



