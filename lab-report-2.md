# Week 4 Lab Report 2 

## Github Code Change #1
By adding in 
<img width="1272" alt="Screen Shot 2022-04-23 at 5 52 46 PM" src="https://user-images.githubusercontent.com/98505287/164951041-73314e75-82fa-41fb-a823-ac39a4671df9.png">


## Link to test file for failure-inducing input
[Link to testone.md](https://github.com/briifernandez/markdown-parser/blob/main/testone.md)


## Symptom of failure-inducing input & commit message history
Output at command line:
<img width="751" alt="Screen Shot 2022-04-23 at 5 49 51 PM" src="https://user-images.githubusercontent.com/98505287/164951119-35907d77-29ae-4879-8b5c-453d1193c338.png">

Commit message history:
<img width="1231" alt="Screen Shot 2022-04-23 at 5 55 30 PM" src="https://user-images.githubusercontent.com/98505287/164951103-56c751eb-9ad1-4864-8705-0f7fbfc601f6.png">


## Relationship between bug, symptom, & failure-inducing input
The bug at this current stage of the program is within the `public static ArrayList<String> getLinks(String markdown)` method, which contains a while loop that has no conditions to cause a break in the loop. After running test-file.md, we can see that the symptom would be the oscillating values of 0, 39, 64 when printing out `currentIndex`. By causing a failure-inducing input that is `[link1][https://user-images.githubusercontent.com/98505287/162337720-6de440da-070c-43e7-86a1-0297fe5fe74e.png]` which contains only brackets, we can see that there would also be the symptom of having an StringIndexOutOfBoundsException.




[Link to my site :)](https://briifernandez.github.io/cse15l-lab-reports/index.html) 
