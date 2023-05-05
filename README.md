Download Link: https://assignmentchef.com/product/solved-cse110-module7-die
<br>
Your client is developing a new Java class library to support group games. As lead developer, you have been tasked to design and implement one of the most fundamental classes in this library: Die (singular of <em>Dice</em>). Typically, the Dice we are familiar with is a cube with the values 1 through 6 on different faces. When rolled, the Die lands randomly showing one of the faces up, i.e. its “value”. Your client wants a more general Die that can represent a shape with any number of sides (&gt; 1). Further, a Die can be “frozen” which will prevent its value from changing, even if someone tries to set its value or roll it.

In addition to writing the Class Die, you will need to write a test driver program to prove that the Die Class operates correctly. See the Required Test cases below, and the sample output.

<h1>2. Class Definition</h1>

<em>Constructors (all public) </em>

<u>Die(int numSides)</u>: Creates a new, unfrozen Die with the given number of sides and initial value of 1. Ensure that the number of sides &gt; 1. If not, print a message and assume 6 sides.

<u>Die()</u>: Creates a new Die with 6 sides by using the constructor above.

<em>Accessors/Mutators </em><u>public void setValue(int v)</u>: Set the value of the Die, if the status is not frozen. If the Die is frozen, ignore this request, without a message. Ensure that the value is compatible with the number of sides (0 &lt; v &lt;= numSides). If not, print a message and set the value to 1.

<u>public int getValue()</u>: Return the value of the Die.

<em>Functions </em><u>public void roll()</u>: “Roll the Die” and set the value to the resulting value. If the Die is frozen, ignore this request, without a message. The resulting value should be between 1 and number of Sides, inclusive.

<u>public void print()</u>: Print a simple graphic for the Die: “[<em>n</em>:<em>x</em>]”, where <em>n</em> is the value, <em>x</em> is the number of sides.

<u>public void draw()</u>: If the number of sides &lt;= 6, print a more realistic graphic for the Die. If the number of sides &gt; 6, default to print(). The example for 5 is shown below:

…….

.     .

. * * .

.  *  .

. * * .

.     .

…….

<u>public void freeze()</u>: Set the status of the die so that it will not change value (Set setValue and roll).

<u>public void unfreeze()</u>: Set the status of the die so that it is allowed to change value (See setValue and roll).

<h1>3. Notes</h1>

<ul>

 <li>I would suggest two classes: Die, and DieDriver (required). DieDriver will test Die by implementing the tests required below in “Required Test Cases”.</li>

 <li>Use plenty of print statements in your output so the grader can understand the test you are running.</li>

 <li>The Test Cases marked with an asterisk (*) should produce an error and keep going.</li>

 <li>Turn in only your source files.</li>

 <li>Because this program includes the verification built in, your verification table should match the tests and identify the expected output for each.</li>

</ul>

<ol start="4">

 <li><strong>Required Main Class </strong></li>

</ol>

DieDriver

<ol start="5">

 <li><strong>Required Input </strong></li>

</ol>

None

<h1>6. Required Test Cases</h1>

<ol>

 <li>Test the creation of Dice. Create and print each (d1, d2, d3) of the following Dice:

  <ol>

   <li>d1: Create a default Die, print it</li>

   <li>d2: Create a die with 4 side, print it</li>

   <li>d3: Create a die with 10 sides, print it</li>

  </ol></li>

 <li>Test setting the value of Dice. Set the value and print the following Dice:

  <ol>

   <li>d1: set to 3, print it</li>

   <li>*d2: set to 5, print it</li>

   <li>*d3: set to 0, print it</li>

  </ol></li>

 <li>Test freezing a Die. Set the value and print the following Dice:

  <ol>

   <li>d1: freeze it, set the value to 5, print it</li>

   <li>d1: unfreeze it, set the value to 5, print it</li>

  </ol></li>

 <li>Test drawing a Die. Draw the following Dice:

  <ol>

   <li>d1: Draw it</li>

   <li>d2: Draw it</li>

   <li>d3: Draw it</li>

  </ol></li>

 <li>Test rolling a Die.

  <ol>

   <li>d1: Roll and print it 10 times.</li>

   <li>d2: Roll and print it 3 times.</li>

   <li>d3: Roll and print it 10 times.</li>

  </ol></li>

</ol>

<h1>7. Required Output</h1>

Your output should look something like the following example. It should include your name and a well-documented set of tests, as required above.

Note that <u>your</u> numbers rolled will likely be different, since this is based on random numbers.




Die Driver – E. Eckert




<ol>

 <li>Creation of Die</li>

</ol>




<ol>

 <li>[1:6]</li>

 <li>[1:4]</li>

 <li>[1:10]</li>

</ol>




<ol start="2">

 <li>Setting Value of Die</li>

</ol>




*** Attempted to set value to 5, assumed 1. *** Attempted to set value to 0, assumed 1.

<ol>

 <li>[3:6]</li>

 <li>[1:4]</li>

 <li>[1:10]</li>

</ol>




<ol start="3">

 <li>Freezing a Die</li>

</ol>




<ol>

 <li>[3:6]</li>

 <li>[5:6]</li>

</ol>




<ol start="4">

 <li>Drawing a Die

  <ol>

   <li>…….</li>

  </ol></li>

</ol>

.     .

. * * .

.  *  .

. * * .

.     .

…….




<ol>

 <li>…….</li>

</ol>

.     .

.     .

.  *  .

.     .

.     .

…….




<ol>

 <li>[1:10]</li>

</ol>




<ol start="5">

 <li>Rolling a Die

  <ol>

   <li>[6:6] [5:6] [5:6] [6:6] [2:6] [2:6] [5:6] [3:6] [2:6] [2:6]</li>

   <li>[4:4] [1:4] [3:4]</li>

   <li>[9:10] [7:10] [3:10] [6:10] [10:10] [6:10] [5:10] [2:10] [5:10] [2:10]</li>

  </ol></li>

</ol>


