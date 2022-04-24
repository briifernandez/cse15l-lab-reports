# Week 4 Lab Report 2 

## Github Code Change #1
Code Change: By adding in `if(openBracket == -1) {break;}`, we can see progress in fixing the bug as it stops producing the StringIndexOutOfBoundsException. Instead after testing testone.md with this change, it produces the output of 0 for currentIndex and [].
<img width="968" alt="Screen Shot 2022-04-23 at 6 34 44 PM" src="https://user-images.githubusercontent.com/98505287/164951981-d054d42a-f914-4449-a2f4-0d74da455254.png">


### Link to test file for failure-inducing input
[Link to testone.md](https://github.com/briifernandez/markdown-parser/blob/main/testone.md)


### Symptom of failure-inducing input & commit message history
Output at command line:
<img width="751" alt="Screen Shot 2022-04-23 at 5 49 51 PM" src="https://user-images.githubusercontent.com/98505287/164951119-35907d77-29ae-4879-8b5c-453d1193c338.png">

Commit message history:
<img width="1231" alt="Screen Shot 2022-04-23 at 5 55 30 PM" src="https://user-images.githubusercontent.com/98505287/164951103-56c751eb-9ad1-4864-8705-0f7fbfc601f6.png">


### Relationship between bug, symptom, & failure-inducing input
The bug at this current stage of the program is within the `public static ArrayList<String> getLinks(String markdown)` method, which contains a while loop that has no conditions to cause a break in the loop. After running test-file.md, we can see that the symptom would be the oscillating values of 0, 39, 64 when printing out `currentIndex`. By causing a failure-inducing input that is `[link1][https://user-images.githubusercontent.com/98505287/162337720-6de440da-070c-43e7-86a1-0297fe5fe74e.png]` which contains only brackets, we can see that there would also be the symptom of having an StringIndexOutOfBoundsException.

////////
## Github Code Change #2
Code Change: After the failure inducing output, the currentIndex was still oscillating infinitely. To fix this symptom, adding `if(openParen == -1 || openBracket == -1) {break;}` results in the output of 0 for currentIndex and [].
<img width="977" alt="Screen Shot 2022-04-23 at 7 02 08 PM" src="https://user-images.githubusercontent.com/98505287/164952634-8c55c84e-cae6-4f91-849a-6c5a53dae675.png">



### Link to test file for failure-inducing input
[Link to testtwo.md](https://github.com/briifernandez/markdown-parser/blob/main/testtwo.md)


### Symptom of failure-inducing input & commit message history
Output at command line:
<img width="533" alt="Screen Shot 2022-04-23 at 6 39 44 PM" src="https://user-images.githubusercontent.com/98505287/164952063-91c2c8fd-097a-4b75-9857-4796a7e830eb.png">

Commit message history:
<img width="900" alt="Screen Shot 2022-04-23 at 6 43 44 PM" src="https://user-images.githubusercontent.com/98505287/164952132-cde0493a-6879-44bf-b678-d3e07cf6029a.png">

### Relationship between bug, symptom, & failure-inducing input
The bug was fixed for failure-inducing input one by having the `openParen == -1` as the condition for a break in the while loop, however for a failure-inducing input that has only parentheses, it caused the bug(insufficient conditions for the while loop) to persist since different conditions can also cause a while loop to continue. For the failure-inducing input in testtwo.md, it is an input with only parentheses and is far apart in the file. After running the file in the command line, the symptom resulting in currentIndex having the value of 44 infinitely, which is from the bug being executed.  

## Github Code Change #3


[Link to my site :)](https://briifernandez.github.io/cse15l-lab-reports/index.html) 


