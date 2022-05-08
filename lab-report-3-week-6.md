# Week 6 Lab Report 3 

## Streamlining ssh Configuration
`.ssh/config` **file**:
To create the config file that will allow us to ssh by using an alias, I had first used the command `cd .ssh` in order to change my directory into the .ssh directory. Then, I used the command `vim config` to create config as a new file. I procceded to press `i` which allows us to insert text into the file directly in the terminal. When all the text is typed out, I pressed `esc` then typed `:wq` which saves the text and exits. After the Host, I choose the alias briana. 

<img width="390" alt="Screen Shot 2022-05-06 at 8 03 49 PM" src="https://user-images.githubusercontent.com/98505287/167235747-af4a2c01-5efd-4572-89da-d5cfd26590ae.png">


`ssh` **command**:
To ssh into our account on the remote server, I simply typed `ssh briana` which is a more efficient way in accessing our account! The config file allows us to proceed without using our account name. 

<img width="564" alt="Screen Shot 2022-05-06 at 8 04 37 PM" src="https://user-images.githubusercontent.com/98505287/167235765-86ae55f1-448b-4d96-92eb-0e43a00f2f6d.png">

`scp` **command**:
Originally, the `scp` command would require our account name, but instead we can copy a file onto our account by typing `scp filename alias:~/`. We can see that the file is in our account by typing `ls`.

<img width="808" alt="Screen Shot 2022-05-06 at 8 07 11 PM" src="https://user-images.githubusercontent.com/98505287/167235771-dee53836-0c19-4a56-b117-be64360954a9.png">






---
## Setup GitHub Access from ieng6

**public key stored on Github:**


**public key stored on user account:**



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
