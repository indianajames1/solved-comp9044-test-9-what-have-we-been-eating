Download Link: https://assignmentchef.com/product/solved-comp9044-test-9-what-have-we-been-eating
<br>
These questions must be completed under self-administered exam-like conditions. You must time the test yourself and ensure you comply with the conditions below.

You may complete this test in CSE labs or elsewhere using your own machine.

You may complete this test at any time before Thursday 06 August 21 00.

Weekly tests are designed to act like a past paper – to give you an idea of how well you are progressing in the course, and what you need to work on. Many of the questions in weekly tests are from past final exams.

Once the first hour has finished, you must submit all questions you’ve worked on.

You should then take note of how far you got, which parts you didn’t understand.

You may choose then to keep working and submit test question anytime up to Thursday 06 August 21 00 However the maximum mark for any question you submit after the first hour will be 50%

You may access this language documentation while attempting this test:

<a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/resources/cheatsheets/shell-perl-qrc.pdf">Shell</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/resources/cheatsheets/shell-perl-qrc.pdf">/</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/resources/cheatsheets/shell-perl-qrc.pdf">Re</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/resources/cheatsheets/shell-perl-qrc.pdf">g</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/resources/cheatsheets/shell-perl-qrc.pdf">ex</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/resources/cheatsheets/shell-perl-qrc.pdf">/</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/resources/cheatsheets/shell-perl-qrc.pdf">Perl</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/resources/cheatsheets/shell-perl-qrc.pdf">quick</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/resources/cheatsheets/shell-perl-qrc.pdf">reference </a><a href="https://cgi.cse.unsw.edu.au/~cs2041/doc/perldoc-html-5.14.0/index.html">full Perl</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/doc/perldoc-html-5.14.0/index.html">d</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/doc/perldoc-html-5.14.0/index.html">o</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/doc/perldoc-html-5.14.0/index.html">cumentation</a>

You may also access manual entries (the man command).

Any violation of the test conditions will results in a mark of zero for the entire weekly test component.

Set up for the test by creating a new directory called test09, changing to this directory, and fetching the provided code by running these commands:

$ <strong>mkdir test09</strong>

$ <strong>cd test09</strong>

$ <strong>2041 fetch test09</strong>

Or, if you’re not working on CSE, you can download the provided code as a <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/test/09/provided.zip">zip</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/test/09/provided.zip">file</a> or a <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/test/09/provided.tar">tar</a> <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/test/09/provided.tar">file</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/test/09/provided.tar">.</a>

Write a Perl program distinct_lines.pl which given a single argument n reads lines from standard input until n different lines have been read.

It should then print a message (exactly as below) indicating how many lines were read. It should then stop. It should not read futher input

If end-of-input is reached before n different lines it should print a message indicating how many lines were read.

Your program should ignore case and white-space when comapring lines.

You can assume your program is given a single positive integer as argument.

<table width="961">

 <tbody>

  <tr>

   <td width="961">$ <strong>./distinct_lines.pl 3</strong> <strong>hi hello world hi hello world hello world bye </strong>3 distinct lines seen after 6 lines read.</td>

  </tr>

  <tr>

   <td width="961">$ <strong>./distinct_lines.pl 3</strong> <strong>hi hello world    hi </strong><strong>hello        world    HELLO  world bye </strong>3 distinct lines seen after 6 lines read.</td>

  </tr>

  <tr>

   <td width="961">$ <strong>./distinct_lines.pl 4</strong> <strong>how are you are how are well </strong>4 distinct lines seen after 7 lines read.</td>

  </tr>

  <tr>

   <td width="961">$ <strong>./distinct_lines.pl 3</strong> <strong>how are you </strong>3 distinct lines seen after 3 lines read.</td>

  </tr>

  <tr>

   <td width="961">$ <strong>./distinct_lines.pl 7</strong> <strong>hello how are you </strong><em>Ctrl-D                      </em>End of input reached after 4 lines read – 7 different lines not seen.</td>

  </tr>

 </tbody>

</table>

No error checking is necessary.

When you think your program is working you can autotest to run some simple automated tests:

$ <strong>2041 autotest distinct_lines</strong>

When you are finished working on this exercise you must submit your work by running give:

$ <strong>give cs2041 test09_distinct_lines distinct_lines.pl</strong>

Your task is to write a Shell script eating.sh which prints a list of the food we have bought at the supermarket in the last week.

It will be given as its first argument a file containing a list of supermarket bills.

The file will be in this format:

[

[

{“name”: “Rice”, “price”: “$4.29”},

{“name”: “Butter”, “price”: “$4.00”}

],

[

{“name”: “Cheese”, “price”: “$8.82”},

{“name”: “Rice”, “price”: “$6.84”},

{“name”: “Pasta”, “price”: “$7.87”}

],

[

{“name”: “Peanut Butter”, “price”: “$6.93”},

{“name”: “Bread”, “price”: “$3.32”},      {“name”: “Noodles”, “price”: “$4.71”}

],

[

{“name”: “Cheese”, “price”: “$4.60”},      {“name”: “Rice”, “price”: “$8.23”},

{“name”: “Bread”, “price”: “$5.99”},

{“name”: “Pasta”, “price”: “$0.54”},

{“name”: “Ramen”, “price”: “$0.98”}

],

[

{“name”: “Noodles”, “price”: “$0.38”}

]

]

If eating.sh was given this file as its first argument it should print

Bread

Butter

Cheese Noodles

Pasta

Peanut Butter

Ramen

Rice

bills.json contains an example list of bills

Download <a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/eating/bills.json">bills</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/eating/bills.json">.</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/eating/bills.json">j</a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/eating/bills.json">son</a>, or copy it to your CSE account using the following command:

$ <strong>cp -n /web/cs2041/20T2/activities/eating/bills.json .</strong>

Here is how eating.sh should behave:

<table width="961">

 <tbody>

  <tr>

   <td width="961">$ <strong>eating.sh bills.json</strong>BreadButterCheese NoodlesPastaPeanut ButterRamenRice</td>

  </tr>

 </tbody>

</table>

You must print the food in alphabetic order.

Each type of food must be printed only once.

Your function does not have to handle differences in case or white-space.

You can assume the formating of the file is the same as the example above. Your program does not have to handle the many other ways a JSON file might be formatted.

You can assume the “name” and “price” fields are always in the same order as the above example. Your answer must be Shell. You can not use other languages such as Perl, Javascript, Python or C.

No error checking is necessary.

When you think your program is working you can autotest to run some simple automated tests:

$ <strong>2041 autotest eating</strong>

When you are finished working on this exercise you must submit your work by running give:

$ <strong>give cs2041 test09_eating eating.sh</strong>

Your task is to write a Perl program json_count.pl which takes as its first argument a whale species and its second argument a file containing a list of whale observations, and prints the number of whales of that species in the file.

The file will be in this format:

[

{

“date”: “09/09/18”,

“how_many”: 11,

“species”: “Orca”

},

{

“date”: “04/11/17”,

“how_many”: 41,

“species”: “Long-finned pilot whale”

},

{

“date”: “17/03/18”,

“how_many”: 30,

“species”: “Southern right whale”

},

{

“date”: “17/08/18”,

“how_many”: 31,

“species”: “Orca”

}, ]

If json_count.pl was given “Orca” as its first argument and the above file as its second argument , it should print 42.

For example:

$ <strong>./json_count.pl Orca whales.json</strong>

117

$ <strong>./json_count.pl ‘Striped dolphin’ whales.json</strong>

19

$ <strong>./json_count.pl ‘Southern right whale’ whales.json</strong>

64

$ <strong>./json_count.pl ‘Whale Shark’ whales.json</strong>

0

You can assume the formating of the file is the same as the example above. Your program does not have to handle the many other ways a JSON file might be formatted.

You can assume the “date”, “how_many” and “species” fields in whale observations are always in the same order as the above example.

Your answer must be Perl only. You can not use other languages such as Shell, Python or C.

You may not run external programs, e.g. via system or backquotes.

You may use any Perl module installed on CSE systems.

No error checking is necessary.

When you think your program is working you can autotest to run some simple automated tests:

$ <strong>2041 autotest json_count</strong>

When you are finished working on this exercise you must submit your work by running give:

$ <strong>give cs2041 test09_json_count json_count.pl</strong>