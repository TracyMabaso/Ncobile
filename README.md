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


EXERCISE 2 :VISUALIZING LEARNING PROGRESS ANSWERS 

Q1: Why do the errors go up and down (like 2, 1, 2, 1) before stopping at 0?
The mistakes go up and down because, at the beginning, the Perceptron is still learning and changing its rules.  
Every time it fixes one wrong guess, that change might cause it to get another guess wrong.  
This back-and-forth fixing keeps happening until the Perceptron figures out the right rule to split the books into two groups.

Q2: What does it mean when the mistakes stop at 0? 
When the mistakes go down to zero, it means the Perceptron has learned the perfect rule to tell the difference between fiction and non-fiction books.  
It’s like a robot librarian that now knows exactly how to sort every book without messing up.  
It has found the right line to split the two types of books, so it doesn’t need to change its rules anymore.


Exercise 3: Visualizing the Decision Boundary

Q1: Where is the new book [3, 2] placed compared to the decision line? Does this explain the -1 guess?
The new book [3, 2], shown as a green star, is sitting in the red-colored area on the picture.  
This red area mean non-fiction(real stories), which is marked as -1.  
That’s why the Perceptron gave a guess of -1 the book is on the non-fiction side of the dividing line.


Q2: How does the decision line split the fiction and non-fiction books?
The decision line is a straight line that cuts the space into two parts:  
- One part is blue, which means fiction (+1)  
- The other part is red, which means non-fiction (-1)  

On the blue side, all the fiction books (shown as blue circles) are grouped together.  
On the red side, all the non-fiction books (shown as red Xs) are grouped together.  
This shows the data is easy to split using a straight line.


Q3: If you move the new book to [4, 4], what guess would you expect? Why?**  
If the book is moved to [4, 4], it would land in the blue-colored area on the picture.  
So, the Perceptron would guess it is fiction(+1).  
This is because [4, 4] is on the same side of the line as the other fiction books


Exercise 4: Experimenting with Parameters:

Q1 :How does changing eta (learning speed) affect learning?  
When eta is small (like 0.01), the Perceptron takes tiny, careful steps While learning.  
It might need more practice rounds, but it learns smoothly and makes no mistakes in the end.  
When eta is big (like 0.5), the steps are large, so it can learn faster sometimes.  
But big steps can also jump too far and make it hard to settle down, so it might not learn properly.

Q2: How does changing n_iter (practice rounds) affect learning? 
More practice rounds give the Perceptron more time to fix its wrong guesses.  
This usually helps it finish learning well.  
If there are fewer rounds, it might stop too soon, before it finds the best rule  
This is especially true when eta is big, and the updates move around too much

Q3: Why do the two settings give different guesses for the same new book [3, 2]?  
They give different guesses because the final rules (called weights) are not the same.  
The slow setting trains for longer and finds a rule that puts [3, 2] in the non-fiction group (-1).  
The fast setting stops after only 5 rounds, so it hasn’t fully learned yet.  
Its rule still puts [3, 2] in the fiction group (+1)

Exercise 5: Trying a New Dataset:

Q1: What does the prediction mean (Setosa or Versicolor)
- Minus one means Setosa  
- Plus one means Versicolor
This shows that the Perceptron gives a result of plus one for the point [4.0, 1.0], so it thinks the flower is Versicolor.

 Q2: Does the list of mistakes go down to zero?

The list of mistakes shows how many wrong guesses the Perceptron makes in each round.
For the first 100 flowers (Setosa and Versicolor), the data can be split with a straight line. That means the Perceptron can learn to guess correctly every time.
So yes, the mistakes can go down to zero if the Perceptron gets enough practice.
If the mistakes don’t go away, it might be because:
- There are not enough practice rounds (n_iter is 10)  
- The learning speed is too slow (eta is 0.1)

Q3: How does the decision line look in the Iris data compared to the book data?
In the Iris flower data, the decision line is straight and clean. It separates Setosa and Versicolor very well.
In the book data, the points might be mixed or messy. The line might not be perfect and could make some wrong guesses.
The Perceptron works best when the data can be split with a straight line.


Bonus Challenge Answers:

A. What happens when you add a new book [3, 4] with label plus one?
If you add the new point [3, 4] with label plus one and train the Perceptron again, the decision line might move a little to fit the new point.
Because of this, the guess for [3, 2] might change. The Perceptron tries to make the best rule for all the points.

B. What happens when you change random_state (like 42 or 100)?

The random_state changes the order of the training points. That means the Perceptron sees the points in a different order each time.
This can change how many mistakes happen in each round, because the updates happen differently.
But if the data can be split with a straight line, the final guesses usually stay the same.













