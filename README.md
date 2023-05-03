Download Link: https://assignmentchef.com/product/solved-cs1027-lab6
<br>
<ul>

 <li>Implement missing methods in a queue made with a Linked List structure</li>

 <li>Use the queue collection to track cyclical movement patterns</li>

 <li>Consider and compare the implications of using different implementations of queues  Observe the results of a simulated snail race!</li>

</ul>

<h1>Pre-Lab</h1>

<ul>

 <li>Create a new Java project called Lab6</li>

 <li>Download the files: <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/QueueADT.java">java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/QueueADT.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/LinkedQueue.java">LinkedQueue.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/LinkedQueue.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/LinearNode.java">LinearNode.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/LinearNode.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/EmptyCollectionException.java">EmptyCollectionException.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/EmptyCollectionException.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/TestQueue.java">TestQueue.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/TestQueue.java">,</a> <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/Snail.java">Snail.java</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/Snail.java">,</a> and <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab06/SnailRace.java">SnailRace.java</a>  Save these downloaded files into the Lab6 src folder</li>

</ul>

<h1>Exercise 1 – Completing the Linked Queue class</h1>




<ol>

 <li>Open LinkedQueue.java and TestQueue.java and examine the code in both classes.</li>

 <li>Note that LinkedQueue is not complete; all its methods (other than the constructor) are left empty. Without adding any additional instance variables or methods, complete the six empty methods given the following instructions:

  <ul>

   <li>enqueue() – take in an element of the generic type. Create a new LinearNode with the given input element. Make all the proper connections including special ones if this is going to be the first element of the queue. Update count as well.</li>

   <li>dequeue() – if the queue is empty, throw an EmptyCollectionException. If not, retrieve the element at the front of the queue and remove it and then return it. Remember to update the front pointer when this element is being removed and if this is the only item then update rear as well. Decrement count to indicate this removed item.</li>

   <li>first() – if the queue is empty, throw an EmptyCollectionException. If not, retrieve the element at the front of the queue and return it without removing it.</li>

   <li>isEmpty() – return true if there are no elements, and false otherwise.</li>

   <li>size() – return the number of elements in the queue.</li>

   <li>toString() – if the queue is empty, return “The queue is empty.” Otherwise return a single-line string starting with “Queue: ” and then containing all the elements of the queue. There must be a comma and space between elements but the last element must end with a period instead. i.e.</li>

  </ul></li>

</ol>

Queue: 1, 2, 3, 4, 5.

Hint: how can you determine whether a node is the last element?

<ol start="3">

 <li>Run the TestQueue file. This will test that the LinkedQueue methods were properly implemented. If any of the test failed, fix the corresponding methods in LinkedQueue until all the tests pass. You may add print lines in LinkedQueue to help with the debugging. Do not add print lines in TestQueue or alter this file in any way.</li>

</ol>




<h1>Exercise 2 – Completing the Snail class</h1>




<em>Before you begin this exercise, read this overview to explain what you’re working on. You’ll be simulating a snail race using queues that contain the snails’ movement patterns. These queues will need to cycle so that the pattern continues repeatedly until the race is over. </em>




<ol>

 <li>Open Snail.java and SnailRace.java and examine the code. Note that the methods in Snail.java are empty. This class is used for representing each of the snails in the race.</li>

 <li>Complete the constructor:

  <ul>

   <li>initialize the snail’s position to 0</li>

   <li>initialize the snail’s queue “movePattern” and add each of the step sizes from the int array to the snail’s queue in the same order they come in the array</li>

  </ul></li>

 <li>Complete the move() method:

  <ul>

   <li>dequeue the first move pattern number and store it in a variable</li>

   <li>re-enqueue this movement to the back of the queue so it will cycle around</li>

   <li>increment the snail’s position by the move pattern value</li>

   <li>don’t let the snail go <strong>past</strong> the finish line; after the movement, check its position compared to the race length (this is a variable in the SnailRace class so examine how the variable was made to determine how you can access it from here) and just leave it at the finish line if was going to be past the line</li>

  </ul></li>

</ol>




Questions: Consider the possibility of using an Array Queue or a Circular Array Queue instead of the Linked Queue being used in this simulation. Would the simulation’s results be impacted by switching to a different Queue implementation? Which of these classes/methods would you have to modify if you were going to use one of the other queue implementations?




<table width="115">

 <tbody>

  <tr>

   <td colspan="2" width="115">getPosition()</td>

  </tr>

  <tr>

   <td width="79">display()</td>

   <td width="35"> </td>

  </tr>

 </tbody>

</table>

<ol start="4">

 <li>Complete the method to simply return (get) the position 5. Complete the method:

  <ul>

   <li>create two int variables called “dashesBefore” and “dashesAfter” and assign them the values that represent the distance before and after the snail, i.e. when</li>

  </ul></li>

</ol>

the snail is at the start, dashesBefore is 0 and dashesAfter is 50. If the snail moves up 1 space, dashesBefore is 1 and dashesAfter is 49, etc.

<ul>

 <li>use the dashesBefore value to help in displaying that number of dashes on a single line (use System.out.print() rather than .println() to avoid new lines)</li>

 <li>display the snail’s shell using the icon variable (@)</li>

 <li>use the dashesAfter value to display the dashes to the right of the snail icon (all on one line still)</li>

 <li>finally print out a newline character so the next snail’s path will be on a different line than this one</li>

</ul>

<ol start="6">

 <li>When you have completed the Snail.java methods, go into SnailRace.java and run it. Watch the live race in the console (you may need to resize the console to clearly watch the race unfold)</li>

 <li>Experiment with different movement patterns for the snails and you can even add more snails to the race. This is all done in the SnailRace constructor.</li>

</ol>




<em>Screenshot of a simulated snail race about halfway through the race: </em>