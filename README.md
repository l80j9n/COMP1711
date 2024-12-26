java c Module code
UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING
Resit Assessment Brief
Procedural Programming
COMP1711
Resit – Carbon Capture Data Analysis
You should spend around 10-15 hours on this assessment. 100%
Via Gradescope.
Automated feedback through Gradescope
Amy Brereton
   Module title
      Assignment title
   This is a programming assignment. You will design and create a number of programs to solve a problem from your client.
  You are doing this assessment to develop your skills in software design and development.
    Assignment type and description
    Rationale
  Word limit and guidance
   Weighting
      Submission deadline
9th August 2024 @ 23:59 BST
There are no late submissions permitted.
   Submission method
   Feedback provision
       Learning outcomes
assessed
LO1: select appropriate data types to represent data.
LO2: apply problem solving techniques to develop a programming solution to real world problems.
LO3: design, implement, debug and test procedural programs.
   Module leader
   Other Staff contact
  
 UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING
1. Assignment guidance
Scenario, Struct  tokeniseRecord()
You have been asked to work on a new sustainability project, exploring the effectiveness of new carbon- capture techniques by analysing data files produced by sensors.
The data is stored in comma separated value (csv) files, and each row in the file is in this format:
2023-09-01,08:15,150
 The first column represents the date (in YYYY-MM-DD format).
 The second column represents the time (8.15am in our example).
 The third column represents the units of carbon saved (measured in grams) since the last timestamp.
These files are valid if:
- They contain between 1 and 1000 records (inclusive)
- All carbon readings are positive
- The times and dates are valid
- There are no missing values.
To store this data, one of the other developers on your team has produced a custom struct which you can use to store the information for each row in the file:
typedef struct _CARBON_DATA {
    char date[11];
    char time[6];
    int carbon_units;
} carbonData;
And you have also been given the function tokeniseRecord() which is able to split records into their comma separated values – the README.md in the code folder has a brief explanation of how to use this function.
Development Process
It is recommended that you use Github Codespaces, which gives you access to a Linux virtual machine which can run from any internet connected device.
You should develop your code on a private repository to prevent others from accessing it.
You can also access the University’s virtual Linux desktop via:
https://feng-linux.leeds.ac.uk/
You will need to be running the PulseSecure VPN in order to access Feng: instructions here (you must be logged on to the IT service website to access)
   
 UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING
2. Assessment tasks Task 1: Reading Data
Task 1 marks: 25 Expected time: 1 - 2 hours
To ensure that data can be correctly read in from the files, you will make a simple C program which is able to:
1. Read in the csv file (for this task, always named ‘CarbonData_2023.csv’)
o Youmayassumethatthisfilealwaysexistsandisalwaysvalidfortask1.
2. Store it in a suitably sized and structured array using the provided struct carbonData
3. Write the number of records in the file to the screen in this exact format (234 is just an example):
     Number of records in file: 234
4. Write to the screen the first three rows of the file in the following format:
     2023-09-01/07:30/300
     2023-09-01/07:45/400
     2023-09-01/08:00/600
Note that there are NO SPACES in the output string, each value is separated by a single forward slash ‘/’ with a single newline after each row.
How it’s marked:
All submitted code for all tasks is marked by an autograder which checks that your code meets the requirements from the brief. You will see a selection of tests when you submit your code, but some will not be visible to you.
  Each section is tested separately, and marks are available for each individual test.
SECTION
Reading in a new set of data from CarbonData_2023.csv
Printing out the correct first 3 rows
TASK 1 - TOTAL
MARKS AVAILABLE
2.5 marks
10 marks
25 MARKS
  Reading in the original CarbonData_2023.csv file
  2.5 marks
 Printing out the correct number of records
 10 marks

 UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING
Task 2: Analysing Data Task 2 marks: 40
Expected time: 4 – 5 hours
Now that you have been able to read the data into an appropriate structure, you have been given the task of making a tool to analyse the data to give some useful statistics.
Follow good programming practices by structuring your program into two separate files:
CarbonDataStruct.h – A header file containing includes, the struct and any helper functions you'd like to include – the template includes tokeniseRecord().
CarbonAnalysis.c – A program file containing the code and functions needed to solve the given tasks.
Requirements:
The program should present a simple menu system to the user, offering the following functions:
A: Specify the filename to be imported. Implement error checking to handle incorrect filenames. B: Display the total number of records in the file.
C: Find the date and time of the timeslot with the fewest carbon units saved.
D: Fi代 写COMP1711 、 C++
代做程序编程语言nd the date and time of the timeslot with the most carbon units saved.
E: Calculate the mean carbon units saved across all records in the file.
F: Identify the longest continuous period where the carbon units saved are below 100 grams. Q: Quit the program
When an option is selected, you code should show the correct data and then return to the menu.
You must not use ‘clear()’, ‘cls()’ or any other method which clears the screen – this causes issues with grading.
The data should be printed out in the formats below:
Option Example output
B Total records: 229
C Lowest units: 2023-09-01 14:20
D Highest units: 2023-09-01 18:00
E Mean units: 427
Note: This should be rounded to the nearest integer (1.4 -> 1, 1.5 -> 2)
F Longest period start: 2023-09-01 14:20 Longest period end: 2023-09-01 18:00
If the filename provided is invalid (does not exist/cannot open) – you must exit the program and return the value 1.
You do not need to check that the data inside is valid.
                 
 UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING
How it’s marked:
SECTION
B – Correctly counting records in a file
D – Finding row with highest carbon units
F – Finding the correct period of 31or12or23or59or<0
- A record with a missing or empty field

 UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING
Task 4: Quiz Task 4 marks: 15
Expected time: 1 hour
For this task, you will need to complete the 15 question multiple-choice quiz on Gradescope.
There are 3 sections with 5 multi-choice questions each:
- Questions about a provided piece of C code
- Questions about programming in general
- Questions about code quality
Once you begin the quiz, you have 60 minutes to complete it. You only have one attempt to complete it, so be prepared in a quiet environment where you will be able to focus – you should also ensure you have a stable internet connection and a device with sufficient power for 60 minutes.
You may complete this part of the assignment at any time before the deadline.
This is an assessment, and therefore must be completed independently. You can use any notes or online
resources you would like, but you must not work with other students. How it will be marked:
Each of the 15 questions is worth 1 mark – partial marks are not awarded for questions where you can choose multiple answers.
You will not see your mark or any feedback until after marks are released.
 
 UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING
3. General guidance and study support
Please refer to the module teaching materials in Minerva for any background support.
4. Assessment criteria and marking process
All code is graded solely on functionality – you must ensure that your code follows the brief exactly, and use the feedback from the grader to check that your code is passing the visible tests.
The passing mark for the assessment is 40% - you may obtain this grade through any combination of tasks/parts of tasks.
5. Presentation and referencing
If you use an idea in your solution that you have seen on the Web somewhere then add a comment to the code like this:
// I based this on an idea I found here:
// https://stackoverflow.com/questions/12901021/error-in-c-file-handling
If you use a book or a printed resource then give the author and title:
// I based this on an idea I got from here:
// An Introduction to C and GUI Programming by Simon Long, pages 56-57
This assignment is rated ORANGE for use of generative AI tools – this means that you may use generative AI tools in an assistive capacity, but must not generate any of your final answer directly from a generative AI tool.
You may not give any generative AI tool access to this brief or any part of this brief, nor ask it to write code for you.
You must reference any use of any generative AI by comment in the format below: // I based this on a discussion with ChatGPT
// Prompt: Explain how to import a CSV file in C
6. Submission requirements
Your code must:
- Be in C
- Compile on Linux with the following command: gcc *.c –o task
- Not be inside a subfolder (not in a zip)

 UNIVERSITY OF LEEDS | SCHOOL OF COMPUTING
7. Academic misconduct and plagiarism
Leeds students are part of an academic community that shares ideas and develops new ones.
You need to learn how to work with others, how to interpret and present other people's ideas, and how to produce your own independent academic work. It is essential that you can distinguish between other people's work and your own, and correctly acknowledge other people's work.
All students new to the University are expected to complete an online Academic Integrity tutorial and test, and all Leeds students should ensure that they are aware of the principles of Academic integrity.
When you submit work for assessment it is expected that it will meet the University’s academic integrity standards.
If you do not understand what these standards are, or how they apply to your work, then please ask the module teaching staff for further guidance.
By submitting this assignment, you are confirming that the work is a true expression of your own work and ideas and that you have given credit to others where their work has contributed to yours.
 8. Assessment/ marking criteria grid
   Task
Task 1 Task 2 Task 3 Task 4
Description
Reading Data Analysing Data Presenting Data Multiple choice quiz
Marks available
25 40 20 15
Total 100
                 

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
