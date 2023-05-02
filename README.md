Download Link: https://assignmentchef.com/product/solved-cosc117-homework-6-methods
<br>
<h1>1           Before Getting Started on the Exercises</h1>

Review the class examples we discussed this week and make sure you understand what each command and operation does. Specifically, make sure you understand the concept and syntax of methods, parameters, and return values.

Some of these exercises are simply taking programs you have written before and revising them into a program that uses methods to complete the task. In many cases the number of lines of code is decreased due to the reuse of the method in the main program. For each exercise you will be given the main program that must be used and your task is to develop the methods needed to complete the program.

For each exercise submit the Java code file containing the program and a Word, LibreOffice, or text file containing at least 3 runs of the program.

<h1>2           Exercises</h1>

<ol>

 <li>The first program is to construct a Fahrenheit to Celsius conversion chart that will print out a chart of Fahrenheit to Celsius conversions. The output should look like the following.</li>

</ol>

Fahrenheit               Celsius

-50                      -45.56

-45                      -42.78

-40                      -40.00

-35                      -37.22

-30                      -34.44

-25                      -31.67

-20                      -28.89

-15                      -26.11

-10                      -23.33

-5                      -20.56

0                     -17.78

5                     -15.00

10                      -12.22

15                        -9.44

20                        -6.67

25                        -3.89

30                        -1.11

35                          1.67

40                          4.44

45                          7.22

50                        10.00

55                        12.78

60                        15.56

65                        18.33

70                        21.11

75                        23.89

80                        26.67

85                        29.44

90                        32.22

95                        35.00

100                        37.78

105                        40.56

110                        43.33

115                        46.11

120                        48.89

125                        51.67

130                        54.44

135                        57.22

140                        60.00

145                        62.78

150                        65.56

The main program that you must use is,

<strong>public static void </strong>main(String[] args) { System.out.println(“Fahrenheit                     Celsius”);

<strong>for </strong>(<strong>int </strong>i = -50; i &lt;= 150; i += 5) {

System.out.printf(“%6d              %10.2f
”, i, Celsius(i)); }

}

You need to write the method Celsius that takes in a single parameter, a double data type, of the Fahrenheit temperature and return the corresponding Celsius temperature, also a double data type. The conversion formula for Fahrenheit to Celsius is

where <em>C </em>is the Celsius temperature and <em>F </em>is the Fahrenheit temperature.

<ol start="2">

 <li>Most computer games use physics engines to take care of many aspects of game play. The most work that a physics engine usually does in a game is collision detection. Determining when the user (or object) hits a wall, when the laser blast or bullet in a FPS hits a target, etc. Collision detection is a fairly difficult problem to solve and is beyond the scope of this class, but another, more accessible, use of a physics engine in a game is to apply gravity to an object.</li>

</ol>

You have probably seen this in high school physics or possibly as an example in a mathematics class like Calculus. If not, we will discuss the equation fully. Say you take an object, like a tennis ball or small rock, and through it up into the air. The object will have a particular height off the ground at any time after you toss it until it eventually hits the ground. The object will increase in height, until gravity overcomes its initial velocity, and then it will start to fall to the ground. To find the height of the object at any time <em>t </em>in seconds after you toss the object is given by the equation,

where <em>d </em>is the current height of the object, <em>g </em>is the acceleration of gravity, <em>v</em><sub>0 </sub>is the initial velocity and <em>d</em><sub>0 </sub>is the initial height. The acceleration of gravity on Earth in English units is 32.17405 feet/sec<sup>2</sup>, so velocity is in feet/sec, distance is in feet and time is in seconds. Also note that we usually consider the positive direction as up. So a positive <em>d</em><sub>0 </sub>would indicate that the initial position of the object is above the ground and a positive <em>v</em><sub>0 </sub>would indicate that the initial velocity is in the upward direction. Along these lines, gravity would be pulling the object down and hence the negative sign.

A sample run of the program is below.

Input the Initial Height (in feet): 10

Input the Initial Velocity (in feet/sec.): 25

Time Height

0.0                           10.000

0.1                           12.339

0.2                           14.357

0.3                           16.052

0.4                           17.426

0.5                           18.478

0.6                           19.209

0.7                           19.617

0.8                           19.704

0.9                           19.470

1.0                           18.913

1.1                           18.035

1.2                           16.835

1.3                           15.313

1.4                           13.469

1.5                           11.304

1.6                             8.817

1.7                             6.008

1.8                             2.878

1.9                     Hit the ground.

The main program that you must use is,

<strong>public static void </strong>main(String[] args) {

Scanner keyboard = <strong>new </strong>Scanner(System.in);

System.out.print(“Input the Initial Height (in feet): “);

Double d0 = keyboard.nextDouble();

System.out.print(“Input the Initial Velocity (in feet/sec.): “); Double v0 = keyboard.nextDouble();

<strong>double </strong>d = d0; <strong>double </strong>t = 0;

System.out.println();

System.out.println(” Time Height”);

<strong>while </strong>(d &gt; 0) { d = height(d0, v0, t); <strong>if </strong>(d &gt; 0)

System.out.printf(“%5.1f %15.3f 
”, t, d); <strong>else</strong>

System.out.printf(“%5.1f %20s 
”, t, “Hit the ground.”); t += 0.1;

}

}

You need to write the method height that takes in three parameters all double values. The first is the initial height, the second the initial velocity, and the third is the time. The return value is the current height of the object, also a double data type.

<ol start="3">

 <li>Nice output for a blackjack program. The output of the program is to look like the following.</li>

</ol>

Player 1

Card 1: King of Spades

Card 2: 8 of Spades

Player 2

Card 1: King of Hearts

Card 2: Queen of Clubs

For this program the main must be the following.

<strong>public static void </strong>main(String[] args) { <strong>int </strong>p1f1 = (<strong>int</strong>) (Math.random() * 13) + 1; <strong>int </strong>p1s1 = (<strong>int</strong>) (Math.random() * 4) + 1; <strong>int </strong>p1f2 = (<strong>int</strong>) (Math.random() * 13) + 1; <strong>int </strong>p1s2 = (<strong>int</strong>) (Math.random() * 4) + 1;

<strong>int </strong>p2f1 = (<strong>int</strong>) (Math.random() * 13) + 1; <strong>int </strong>p2s1 = (<strong>int</strong>) (Math.random() * 4) + 1; <strong>int </strong>p2f2 = (<strong>int</strong>) (Math.random() * 13) + 1; <strong>int </strong>p2s2 = (<strong>int</strong>) (Math.random() * 4) + 1;

System.out.println(“Player 1”);

System.out.println(“Card 1: ” + CardString(p1f1, p1s1)); System.out.println(“Card 2: ” + CardString(p1f2, p1s2));

System.out.println();

System.out.println(“Player 2”);

System.out.println(“Card 1: ” + CardString(p2f1, p2s1));

System.out.println(“Card 2: ” + CardString(p2f2, p2s2)); }

You need to create the method CardString that takes in two integer parameters. The first parameter is the face value of the card (1–13 with 1 being the Ace and 11, 12, and 13 being Jack, Queen, and King respectively). The second parameter is the suit value of the card (1–4 which represent Hearts, Diamonds, Clubs, and Spades respectively). The method is to return the string of the card’s value and suit so that the output matches the examples.

<ol start="4">

 <li>High-low game: The output of the program is to look like the following. These are three separate runs.</li>

</ol>

<table width="546">

 <tbody>

  <tr>

   <td width="201">Player 1: 5 of SpadesPlayer 2: Ace of ClubsPlayer 2 Wins</td>

   <td width="201">Player 1: Queen of HeartsPlayer 2: Queen of SpadesPlayer 2 Wins</td>

   <td width="143">Player 1: 8 of ClubsPlayer 2: 8 of Clubs It is a draw.</td>

  </tr>

 </tbody>

</table>

For this program the main must be the following.

<strong>public static void </strong>main(String[] args) { <strong>int </strong>player1CardFace = getCardFace(); <strong>int </strong>player1CardSuit = getCardSuit(); <strong>int </strong>player2CardFace = getCardFace(); <strong>int </strong>player2CardSuit = getCardSuit();

System.out.println(“Player 1: ” + CardString(player1CardFace, player1CardSuit)); System.out.println(“Player 2: ” + CardString(player2CardFace, player2CardSuit)); <strong>int </strong>win = Winner(player1CardFace, player1CardSuit, player2CardFace, player2CardSuit);

<strong>if </strong>(win == 1)

System.out.println(“Player 1 Wins”); <strong>else if </strong>(win == 2)

System.out.println(“Player 2 Wins”); <strong>else</strong>

System.out.println(“It is a draw.”);

}

Copy over your CardString method from the previous exercise, then update it so that the face values go from 2–14 with 11, 12, 13, and 14 being Jack, Queen, King, and Ace respectively. Create the following three methods,

<ul>

 <li>getCardFace() that returns a random number between 2 and 14.</li>

 <li>getCardSuit() that returns a random number between 1 and 4.</li>

 <li>Winner(int p1f, int p1s, int p2f, int p2s) that takes in four parameters, the first two are face value and suit of the card for player 1 and the last two are the face value and suit of the card for player 2. The method should return 1 if player 1 wins, 2 if player 2 wins and 0 if it is a draw. Remember that the rules are that the higher face value wins (with Ace high), if the face values are the same then the suits are compared with Spades winning over Clubs which wins over Diamonds which wins over Hearts.</li>

</ul>

<ol start="5">

 <li>Factorial: The output of the program is to look like the following. These are five separate runs.</li>

</ol>

<table width="503">

 <tbody>

  <tr>

   <td width="201">n = 55! = 120n = 1313! = 6227020800</td>

   <td width="201">n = 2020! = 2432902008176640000n = 0 n! = 1</td>

   <td width="100">n = -3Invalid input!</td>

  </tr>

 </tbody>

</table>

For this program the main must be the following.

<strong>public static void </strong>main(String[] args) {

Scanner keyboard = <strong>new </strong>Scanner(System.in); System.out.print(“n = “); <strong>int </strong>n = keyboard.nextInt();

<strong>if </strong>(n &lt; 0)

System.out.print(“Invalid input!”); <strong>else if </strong>(n == 0)

System.out.print(“n! = 1”); <strong>else</strong>

System.out.print(n + “! = ” + factorial(n));

}

You need to create the method factorial that takes in a long integer parameter <em>n </em>and returns a long with the value of <em>n</em>!.

<ol start="6">

 <li>Double Factorial: The output of the program is to look like the following. These are five separate runs.</li>

</ol>

<table width="503">

 <tbody>

  <tr>

   <td width="201">n = 55!! = 15n = 66!! = 48</td>

   <td width="201">n = 2020!! = 3715891200n = 0 n!! = 1</td>

   <td width="100">n = -3Invalid input!</td>

  </tr>

 </tbody>

</table>

For this program the main must be the following.

<strong>public static void </strong>main(String[] args) {

Scanner keyboard = <strong>new </strong>Scanner(System.in); System.out.print(“n = “); <strong>int </strong>n = keyboard.nextInt();

<strong>if </strong>(n &lt; 0)

System.out.print(“Invalid input!”); <strong>else if </strong>(n == 0)

System.out.print(“0!! = 1”); <strong>else</strong>

System.out.print(n + “!! = ” + doubleFactorial(n));

}

You need to create the method doubleFactorial that takes in a long integer parameter <em>n </em>and returns a long with the value of <em>n</em>!!.

<ol start="7">

 <li>Character Counts: The output of the program is to look like the following.</li>

</ol>

Input a phrase: This is a test.

The A count is 1

The E count is 1

The H count is 1

The I count is 2

The S count is 3

The T count is 3

The most frequent letters are S and T with a count of 3.

For this program the main must be the following.

<strong>public static void </strong>main(String[] args) {

Scanner keyboard = <strong>new </strong>Scanner(System.in);

System.out.print(“Input a phrase: “); String str = keyboard.nextLine(); str = str.toUpperCase();

String MaxCharacters = “”; <strong>int </strong>maxCount = 0; <strong>int </strong>numMax = 0; <strong>int </strong>maxCharsFound = 0; System.out.println();

<strong>for </strong>(<strong>char </strong>ch = ’A’; ch &lt;= ’Z’; ch++) { <strong>int </strong>count = countLetters(str, ch); <strong>if </strong>(count &gt; 0)

System.out.println(“The ” + ch + ” count is ” + count);

<strong>if </strong>(count &gt; maxCount) { maxCount = count;

}

}

System.out.println();

<strong>for </strong>(<strong>char </strong>ch = ’A’; ch &lt;= ’Z’; ch++) { <strong>int </strong>count = countLetters(str, ch);

<strong>if </strong>(count == maxCount) numMax++;

}

<strong>for </strong>(<strong>char </strong>ch = ’A’; ch &lt;= ’Z’; ch++) { <strong>int </strong>count = countLetters(str, ch); <strong>if </strong>(count == maxCount) { MaxCharacters += ch; maxCharsFound++;

<strong>if </strong>(numMax &gt; 1) { <strong>if </strong>(maxCharsFound &lt; numMax – 1)

MaxCharacters += “, “; <strong>else if </strong>(maxCharsFound == numMax – 1) MaxCharacters += ” and “;

}

}

}

<strong>if </strong>(maxCount &gt; 0) { <strong>if </strong>(numMax == 1)

System.out.println(“The most frequent letter is ” + MaxCharacters + ” with a count of ” + maxCount + “.”);

<strong>else</strong>

System.out.println(“The most frequent letters are ” + MaxCharacters + ” with a count of ” + maxCount + “.”);

}

}

You need to create the method countLetters that takes in a string and a character and returns the number of times that character is in the string.