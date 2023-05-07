Download Link: https://assignmentchef.com/product/solved-jac444-workshop-10
<br>









<strong>Description:</strong>

The tasks in this workshop is a recap of some concepts from previous workshops and some new concepts like Comparable Interface and Cloneable Interface.

<strong> </strong>

<strong>Task 1: </strong>

Define a class named <strong>Time</strong> for encapsulating a time. The class contains the following:




<ol>

 <li>A data field of the long time that stores the elapsed time since midnight, Jan 1, 1970.</li>

 <li>A no-arg constructor that constructs a Time for the current time.</li>

 <li>A constructor with the specified hour, minute, and second to create a Time.</li>

 <li>A constructor with the specified elapsed time since midnight, Jan 1, 1970.</li>

 <li>The <strong>getHour()</strong> method that returns the current hour in the range 0-23.</li>

 <li>The <strong>getMinute()</strong> method that returns the current minute in the range 0-59.</li>

 <li>The <strong>getSecond()</strong> method that returns the current second in the range 0-59.</li>

 <li>The <strong>getSeconds()</strong> method that returns the elapsed total seconds.</li>

 <li>The <strong>toString()</strong> method that returns a string such as “1 hour 2 minutes 1 second” and “14 hours 21 minutes 1 second”.</li>

 <li>Implement the Comparable&lt;Time&gt; interface to compare this Time with another one based on their elapse seconds. The compareTo method returns the difference between this object’s elapse seconds and the another’s.</li>

 <li>Implement the Cloneable interface to clone a Time object.</li>

</ol>




Write a test program that produces the following sample run:




Sample Run – 1

Enter time1 (hour minute second): 331 34 674

19 hours 45 minutes 14 seconds

Elapsed seconds in time1: 1194314




Enter time2 (elapsed time in seconds): 93889345

16 hours 22 minutes 25 seconds

Elapsed seconds in time2: 93889345

time1.compareTo(time2)? -92695031

time3 is created as a clone of time1 time1.compareTo(time3)? 0 End Sample Run – 1







Sample Run – 2

Enter time1 (hour minute second): 1 2 3

1 hour 2 minutes 3 seconds

Elapsed seconds in time1: 3723




Enter time2 (elapsed time in seconds): 193032 &lt;Enter&gt;

5 hours 37 minutes 12 seconds

Elapsed seconds in time2: 193032

time1.compareTo(time2)? -189309




time3 is created as a clone of time1

time1.compareTo(time3)? 0

End Sample Run – 2

<strong> </strong>

<strong>Task 2: </strong>

Write a simulation of Banks. Banks trade to other bank by lending and borrowing the money to each other. In tough economic times, if a bank goes bankrupt, it may not be able to pay back the loan.

A bank’s total assets are its current balance plus its loans to other banks.

<ul>

 <li>The diagram below shows five different banks (0 to 4).</li>

 <li>The banks’ current balances are 25, 125, 175, 75, and 181 million dollars, respectively.</li>

 <li>The directed edge from node 1 to node 2 indicates that bank 1 lends 40 million dollars to bank 2.</li>

</ul>







Banks lend money to each other




<ul>

 <li>If a bank’s total assets are under a certain limit, the bank is unsafe.</li>

 <li>The money it borrowed cannot be returned to the lender, and the lender cannot count the loan in its total assets.</li>

 <li>Consequently, the lender may also be unsafe, if its total assets are under the limit.</li>

</ul>




Write a program to find all the unsafe banks. Your program reads the input as follows.

<ol>

 <li>It first reads two integers <strong>n </strong>and <strong>limit</strong>,

  <ol>

   <li><strong>n </strong>indicates the number of banks</li>

   <li><strong>limit </strong>is the minimum total assets for keeping a bank safe from the user.</li>

  </ol></li>

 <li>It then reads <strong>n </strong>lines that describe the information for <strong>n </strong>banks with IDs from <strong>0 </strong>to <strong>n-1</strong>.</li>

</ol>




<ol start="3">

 <li>The first number in the line is the bank’s balance, the second number indicates the number of banks that borrowed money from the bank, and the rest are pairs of two numbers.</li>

</ol>




<ol start="4">

 <li>Each pair describes a borrower. The first number in the pair is the borrower’s ID and the second is the amount borrowed.</li>

</ol>

For example, the input for the five banks in above picture is as follows (<strong>note that the limit is 201</strong>):




Number of banks: 5

Minimum asset limit: 201

<h1>For Bank # 0</h1>

<h2>Balance: 25</h2>

<h2>Number of banks Loaned: 2</h2>

<h3>Bank ID who gets the loan: 1</h3>

Loaned Amount: 100.5

Bank ID who gets the loan: 4

Loaned Amount: 320.5







<h1>For Bank # 1</h1>

Balance: 125

Number of banks Loaned: 2  Bank ID who gets the loan: 2

<h3>Loaned Amount: 40</h3>

Bank ID who gets the loan: 3

Loaned Amount: 85

For Bank # 2  Balance: 175

Number of banks Loaned: 2  Bank ID who gets the loan: 0

Loaned Amount: 125

Bank ID who gets the loan: 3

Loaned Amount: 75

For Bank # 3  Balance: 75

Number of banks Loaned: 1  Bank ID who gets the loan: 0

Loaned Amount: 125

For Bank # 4

<h1>Balance: 181</h1>

Number of banks Loaned: 1  Bank ID who gets the loan: 2

Loaned Amount: 125




The total assets of bank 3 are (75 + 125), which is under 201, so bank 3 is unsafe. After bank 3 becomes unsafe, the total assets of bank 1 fall below (125 + 40). Thus, bank 1 is also unsafe.

<strong>Note: Program should take inputs from the user like Number of banks, Minimum asset limit and then all other inputs </strong>

<strong> </strong>

<strong>The output of the program should be </strong>

Unsafe banks are Bank 3 and Bank 1

Bank 3 got bankrupted and it got the loan from Bank 1, because Bank 3 is unsafe due to under the limit Bank 1 is also unsafe due to lower limit.




<strong> </strong>

<strong> </strong>




<strong> </strong>

Workshop Header




/**********************************************

<strong>Workshop #  </strong>

<strong>Course:</strong><em>&lt;subject type&gt; – Semester </em>

<strong>Last Name:</strong><em>&lt;student last name&gt; </em>

<strong>First Name:</strong><em>&lt;student first name&gt; </em>

<strong>ID:</strong><em>&lt;student ID&gt; </em>

<strong>Section:</strong><em>&lt;section name&gt; </em>

<em>This assignment represents my own work in accordance with Seneca Academic Policy. </em>

<em>Signature </em>

<strong>Date:</strong><em>&lt;submission date&gt; </em>

**********************************************/




<strong> </strong>

Code Submission Criteria:

Please note that you should have:

<ul>

 <li>Appropriate indentation.</li>

 <li>Proper file structure</li>

 <li>Follow java naming convention</li>

 <li>Document all the classes properly</li>

 <li>Do Not have any debug/ useless code and/ or files in the assignment</li>

 <li>Do not have everything in the <em>main method</em>.</li>

 <li>Have a separate TestClass with the main method in it.</li>

 <li>Check your inputs if the user is not entering garbage inputs.</li>

 <li>Use exceptional handling or other methods to let the user know if the inputs are incorrect.</li>

</ul>




Deliverables and Important Notes:




<strong>All these deliverables are supposed to be uploaded on the blackboard once done. </strong>

<strong> </strong>

<ul>

 <li>You are supposed to create video/ record voice/ detailed document of your running solution. <strong>(50%)</strong>  o Screen Video captured file should state your last name and id, like</li>

</ul>

Ali_123456.mp4 (or whatever the extension of the file is) o Record voice clip should also include a separate word file with the screen shots of your program’s output, state your last name and id, like Ali_123456.mp3 (or whatever the extension of the file is)

o Detailed document should include screen shots of your output, have your name and id on the top of the file and save the file with your last name and id, like Ali_123456.docx (or whatever the extension of the file is)

<ul>

 <li>A word/ text file which will reflect on learning of your concepts in this workshop. Also include the instructions on how to run your code.                                 <strong>(30%)</strong>

  <ul>

   <li>Should state your Full name and Id on the top of the file and save the file with your last name and id, like Ali_123456.txt</li>

  </ul></li>

 <li>Submission of working code.                                                                         <strong>(20%)</strong>

  <ul>

   <li>Make sure your follow the “<strong>Code Submission Criteria”</strong> mentioned above.</li>

   <li>You should zip your whole working project to a file named after your Last Name followed by the first 3 digits of your student ID. For example, zip.</li>

  </ul></li>

 <li>Your marks will be deducted according to what is missing from the above-mentioned submission details.</li>

 <li>Late submissions would result in additional 10% penalties for each day or part of it.</li>

 <li>Remember that you are encouraged to talk to each other, to the instructor, or to anyone else about any of the assignments, but the final solution may not be copied from any source.</li>

</ul>






















<strong> </strong>