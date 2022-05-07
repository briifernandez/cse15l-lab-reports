# Week 6 Lab Report 3 

## Streamlining ssh Configuration
`.ssh/config` file:
<img width="390" alt="Screen Shot 2022-05-06 at 8 03 49 PM" src="https://user-images.githubusercontent.com/98505287/167235747-af4a2c01-5efd-4572-89da-d5cfd26590ae.png">
 

`ssh` command:
<img width="564" alt="Screen Shot 2022-05-06 at 8 04 37 PM" src="https://user-images.githubusercontent.com/98505287/167235765-86ae55f1-448b-4d96-92eb-0e43a00f2f6d.png">

`scp` command:
<img width="808" alt="Screen Shot 2022-05-06 at 8 07 11 PM" src="https://user-images.githubusercontent.com/98505287/167235771-dee53836-0c19-4a56-b117-be64360954a9.png">






---
## Github Code Change #2
**Code Change:** After the failure inducing output, the currentIndex was still oscillating infinitely. To fix this symptom, adding `if(openParen == -1 || openBracket == -1) {break;}` results in the output of 0 for currentIndex and [], which fixes the symptom.
<img width="977" alt="Screen Shot 2022-04-23 at 7 02 08 PM" src="https://user-images.githubusercontent.com/98505287/164952634-8c55c84e-cae6-4f91-849a-6c5a53dae675.png">


### Link to test file for failure-inducing input:
[Link to testtwo.md](https://github.com/briifernandez/markdown-parser/blob/main/testtwo.md)


### Symptom of failure-inducing input & commit message history
**Output at command line:**

<img width="533" alt="Screen Shot 2022-04-23 at 6 39 44 PM" src="https://user-images.githubusercontent.com/98505287/164952063-91c2c8fd-097a-4b75-9857-4796a7e830eb.png">

**Commit message history:**

<img width="900" alt="Screen Shot 2022-04-23 at 6 43 44 PM" src="https://user-images.githubusercontent.com/98505287/164952132-cde0493a-6879-44bf-b678-d3e07cf6029a.png">

### Relationship between bug, symptom, & failure-inducing input
The bug was fixed for failure-inducing input one by having the `openParen == -1` condition in the while loop, however for a failure-inducing input that has only parentheses, it caused the bug(insufficient conditions for the while loop) to persist since different conditions can also cause a while loop to continue. For the failure-inducing input in testtwo.md, it is an input with only parentheses and is far apart in the file. By running testthree.md, the symptom resulted in currentIndex having the value of 44 infinitely, which is from the bug being executed.  

---
## Github Code Change #3
**Code Change:** For the final code change, `if(openParen == -1 || openBracket == -1 || closeParen == -1 || closeBracket == -1) {break;}` were the conditions for the while loop in order to create a break in the loop. This fix also resulted in the output of 0 for currentIndex and [], which fixes the symptom, and allows proper formated links to be parsed correctly. The file test-file.md also was fixed and had the output of `[https://something.com, some-thing.html]`.
<img width="976" alt="Screen Shot 2022-04-23 at 7 09 50 PM" src="https://user-images.githubusercontent.com/98505287/164952968-9730c58c-9527-4bbc-8b7d-8cac18b6bbc3.png">

### Link to test file for failure-inducing input:
[Link to testthree.md](https://github.com/briifernandez/markdown-parser/blob/main/testthree.md)

### Symptom of failure-inducing input & commit message history
**Output at command line:**

<img width="734" alt="Screen Shot 2022-04-23 at 7 11 52 PM" src="https://user-images.githubusercontent.com/98505287/164953021-16274f0b-91a7-43dd-b793-1baac2c63b88.png">

**Commit message history:**

<img width="987" alt="Screen Shot 2022-04-23 at 7 12 48 PM" src="https://user-images.githubusercontent.com/98505287/164953062-d9397242-1348-4b70-9a4c-8c77403af9ed.png">

### Relationship between bug, symptom, & failure-inducing input
The bug continued to be the lack of condition statements for the while loop, and after running testthree.md (which contained syntax errors of no close parentheses and no close bracket), it caused the symptom to be a StringIndexOutOfBoundsException. The failure-inducing input causes the bug to execute since `closeParen == -1 || closeBracket == -1` was not included in the condition statements. To fix the failure-inducing input from causing symptoms and to fix this bug from executing, `if(openParen == -1 || openBracket == -1 || closeParen == -1 || closeBracket == -1) {break;}` became the _conditions_ for the while loop. 


[Return to my site's homepage :)](https://briifernandez.github.io/cse15l-lab-reports/index.html) 
