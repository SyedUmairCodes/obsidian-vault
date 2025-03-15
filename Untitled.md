Iterative tasks help you to perform a specific action a definite or known number of times. For example, you want to email a flyer advertising your Java programming skills to a list of 20 recipients. As you have a predefined list of email addresses, you can send a personalized email to each recipient by changing the email address and the recipient's name. This allows you to be consistent and use iterative structures. In this video, you'll learn that in Java, if a code is to be repeated a definite number of times, you can use the for loop as an iterative structure. Imagine Tony bought a robot with an integrated AI named Sidekick. However, to accomplish tasks successfully, Sidekick needs clear, precise, and step-by-step instructions. Tony would love to send Sidekick to go and buy 30 bottles of beer. However, Sidekick can only carry up to five bottles at a time and must make six trips to the store to complete the task. Tony tells Sidekick to check the number of bottles, starting at one and stopping at bottle number 30 to ensure he buys the correct number of bottles. Armed with Tony's credit card details, Sidekick goes shopping while Tony sleeps. Two hours later, Tony wakes up to 195 bottles of beer in Tony's room and a $290 credit card bill. As Sidekick is still buying beer, Tony presses Sidekick's stop button. What went wrong? Tony forgot to tell Sidekick to increment the number of beer bottles for every bottle bought. Therefore, the number of bottles counted for Sidekick always remained at one. Such a mistake is called a logical mistake. It is an expensive logical mistake. Tony learned his lesson during the beer episode and will remember to give Sidekick clear instructions. In preparation for a family get-together, Tony sends Sidekick to buy five turkeys. Sidekick can carry only one turkey at a time. Therefore, Tony writes the following program. Buy one turkey at a time, start counting from zero. Increment the number of turkeys by one each time a turkey was bought and repeat the program five times. Remember, when coding, you start counting at zero. The first turkey Sidekick buys will be number zero. The second turkey number one and the fifth turkey will be number four. Therefore, a total of five turkeys were bought and the program stopped. Tony can use a for loop as the number of repetitions is known. Before we look at how Tony uses a for loop to complete this task, let's look at the structure of a for loop. The structure of the for loop consists of three components, initialize, check and change. Each part separated by a semicolon. Initialize is used to set a value to the variable to count the repetitions in the loop, which is executed only once when the loop starts. Check is a condition to see that the variable value is within the range and if the loop should continue running. Change modifies the variable's value so that the condition fails after the number of repetitions required. Let's return to how Tony needs to program Sidekick only to buy five turkeys. Tony specifies the variable number of turkeys bought inside the for loop with the initial value set to zero. The check indicates the maximum number is less than five. Remember, you have to specify the index number here. The change is made by an increment of one. Tony doesn't want to repeat of the credit card bill episode. Let's run the program. The program ran five times as Tony intended. Java starts counting from zero. Therefore, the plus one simulates human counting. The loop stops when the maximum value of five is reached, indicating that only five turkeys were bought. As Sidekick brought the turkeys home, the number increased by one due to the plus plus or increment operator. If you want the number to decrease by one, use the minus minus or decrement operator. Therefore, the loop will count backward, starting at four and stopping at zero. What is important is that a loop executes for the required number of times. Remember, counting from one and incrementing by one is easier. Let's explore how to change the code to accommodate the decrement operator. The for loop will look different. The initializer is set to five. The check is now greater or equal to one, and the change showcases the decrement operator or minus minus. The print output is changed by removing the plus one. Remember that you want to show a decreasing number of turkeys. The number of repetitions is still five. Now Tony can instruct Sidekick to all kinds of repetitive tasks, freeing up his time and energy for more engaging activities. In this video, you learned how to apply a for loop based on a practical example. You learned that the for loop has three parts, initialize, check, and change. An increase operator can increase the number of turkeys bought, while the decrease operator counts down the number of turkeys bought. This video's key takeaway is that a for loop cannot be used if the number of repetitions is based on a condition. The repetitions need to be based on a definite number.

On weekends, Toni sells ice cream for extra money and wants to efficiently track the number of ice cream scoops sold to manage inventory better. Determining the remaining stock has become repetitive and time-consuming. 

Previously, you learned how to manipulate Strings, employ conditional statements (e.g., **if**, **else**, **else-if**), and a for loop. Conditional statements are used to execute or avoid executing specific pieces of code based on a specified condition that is true or false (Boolean primitive).

From experience, Toni knows that an ice cream container holds 20 scoops. To efficiently keep track of inventory, Toni needs to know how many scoops of ice cream are left in each container **after** a sale. This will help him order new stock on time. 

How does this relate to a Java program? 

You must specify the maximum number of available scoops (e.g., 20) and count **each** until it reaches the specified number of scoops, making the container empty. Therefore, you'll need to use a **for** loop.

When you visit an ATM, there is a menu with options like deposit, withdraw, check your balance, or opt out.
This process continues until you quit.
In Java, you can use iterative structures, like a while loop, to repeat code and create menu systems, like the ATM menu.
In this video, you'll learn how to use while, infinite while, and do-while loops
as iterative structures to repeat code based on a specific condition or user input.
First, let's explore the while loop.
It has the while keyword, a condition, and repetitive code between the curly braces, defining the loop's scope.
When the condition is met, the program stops.
Let's return to Tony and his robot, Psychic.
Tony's latest adventure involves cleaning out the attic and removing all the boxes.
Psychic must move the boxes from the attic to the backyard.
Tony has no idea how many trips it will take Psychic to clean the attic.
The only condition is that Psychic cannot stop until it is clean.
How would you go about coding instructions into Psychic for this task?
Well, the while loop is the perfect solution for a scenario like this, where a task needs to repeat until the job is complete.
Over the next few minutes, you will learn how to code this.
Let's pinpoint the conditions.
One, Psychic can only carry five boxes at a time, and two, the program needs to stop when the attic is clean.
First, you create a variable named totalTrash and assume the initial trash item's value is 22.
The while loop condition indicates that the action should continue while totalTrash is greater than zero.
With each trip, Psychic removes five boxes.
Therefore, each iteration of the loop decreases five items from the collection of junk.
Next, add a message to keep track of the number of remaining boxes.
Let's run this.
After the first cleaning trip, 17 items remained, then 12, and then 7.
So far, so good.
However, after the last trip, it indicates that minus three items remain in the attic, which is obviously a mistake.
It should be zero.
Why did this happen?
Because when the value of totalTrash was two, the condition was still true, causing the loop to repeat one more time, resulting in five being deducted from two.
So, to prevent this, you need to check whether there are five items left for Psychic to carry.
How can you do that?
Oh yes, you can add an if statement.
To modify the code, add a new variable, trashToCarry, with a default value of five, to indicate the items Psychic carries per trip.
Now add an if statement to test if totalTrash is less than five.
If true, the value of trashToCarry should change to the same value of totalTrash.
So, with the next round, the while condition will be false and stop the loop.
Lastly, you should add a print statement to indicate that all the items were cleared.
Awesome.
Psychic cleared the attic as Tony intended, and now the loop stops when the totalTrash is zero.
Next, let's try to create an iterative menu, like the ATM example.
To create something that should continue indefinitely until the user wants to exit the loop, you use a boolean variable.
To keep the loop running, you keep the boolean value true and make it false to stop it.
The while loop syntax stays the same when creating a menu, except the condition will be true until the user decides otherwise.
Say Tony also wants to use Psychic to clean other parts of the house.
The repetitive menu should specify clean the attic, clean the living room, and clean the bedroom.
First, you create the cleaning option variable to store the user's menu choice.
The boolean variable runLoop is set to true and controls the while loop, ensuring that the loop runs at least once.
Next, you insert a while loop.
This loop will continue executing as long as the runLoop condition is true.
Inside the loop, add the repetitive menu.
Prompt the user to enter an integer between 1 and 4 to store the input in the cleaning option variable.
Next, add a switch statement to evaluate the value of the cleaning option variable and execute the corresponding case block.
Insert the fourth option to make the loop exit.
Note that each case ends with a break statement to activate the switch block after executing the code.
For example, if Tony selects 1, case 1 will be executed.
The default option only activates with a selection outside the range of 1 to 4.
Observe that the user can terminate the loop by choosing 4, which changes the value of the variable runLoop to false.
So, the next time the while condition repeats, it reads the false value and stops the loop.
Let's run the code.
The menu displays a repetitive menu.
Say Tony enters 1, which will instruct Cyclic to clean the attic.
Let's test the other values.
2, clean the living room.
3, clean the bedroom.
Finally, when choosing 4, the menu no longer displays and the loop ends.
So far, you've seen how to apply a while loop to repeat an action
and how to create an iterative structure with a boolean variable.
Next, you'll explore the doWhile loop.
The doWhile loop consists of the do keyword followed by the while loop.
The code to be executed is inserted before the while loop,
ensuring it runs at least once and checking the condition after execution.
A typical application of the doWhile loop is when you need to prompt a user at least once,
like when entering a password.
The user is prompted until the correct password is entered.
Let's explore this with an example.
To illustrate this concept, let's assign the variable totalTrashInRoom an initial value of 0.
Add a println statement to display I will take out some trash.
Inside a doWhile loop, we should execute until the value of totalTrashInRoom is greater than 0.
But wait, since the value of totalTrashInRoom is not greater than 0,
you should not get the display, right?
But you will.
Why?
Well, a doWhile checks the condition after executing the code.
Want to test it?
Observe. It executed the code.
In this video, you learned how to apply a while and doWhile loop.
You learned that a while loop runs if a Boolean condition is true.
It is used for repetitive menus.
And a doWhile loop is used to prompt a user at least once.
Repetitive structures like menus are crucial to any software.
They allow humans to interact with the program and dataset.
Mastering the while and doWhile loop is important
whether you plan to develop user interfaces, manage databases,
or implement real-time data processing. 

Do you play triple chance carnival games like Spin the Wheel, Basketball Shootout, Whac-A-Mole, and Balloon Dart Throw? In these games, you get three chances to win a prize, whether you're spinning the wheel or popping a balloon. After three tries, the game ends, and you return to the main menu, replay, or stop.

What do these games have in common with Java? They are classic examples of repetitive questions  and iterative structures for user interactions

In this reading, you'll help Toni write a fun Java program for SideKick using iterative structures like the while loop. You’ll start with simple examples to build a strong foundation and then guide Toni in writing an interactive guessing game program

A while loop allows you to execute a code block repeatedly as long as a certain condition is true. This is useful when you want to keep doing something until a specific condition is met. Let's start with a simple example.

Now that you've seen how a while loop can be used to perform a simple task repeatedly, let's make things more interactive by creating a guessing game. In this game, the computer will choose a secret number, and you'll try to guess it. The loop will keep running until you guess the correct number, making this a fun way to practice while loops.

**Concept of the game**

The idea is simple:

- The computer has a secret number.
    
- The player will keep guessing what that number is from **1** to **9**.
    
- After each guess, the computer will tell you whether your guess was correct or not.
    
- If your guess is wrong, the loop will continue, giving you another chance to guess.
    
- If your guess is right, the loop will stop, and the computer will congratulate you.