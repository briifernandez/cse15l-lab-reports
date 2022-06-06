# Week 10 Lab Report 5 

## Tests with different results:
I was able to find the different results between implementations by using vimdiff which shows the side by side comparisons of the tests. After running make test and bash script.sh > results.txt, I was able to see the differences in the result.txt files.
<img width="650" alt="Screen Shot 2022-06-05 at 7 48 13 PM" src="https://user-images.githubusercontent.com/98505287/172097073-9a88f5a8-6775-4832-b9ef-989a1566fe69.png">
<img width="623" alt="Screen Shot 2022-06-05 at 9 53 02 PM" src="https://user-images.githubusercontent.com/98505287/172097123-9c77bce9-b621-4a08-bb04-54ac8782baa1.png">



## Test file with different results:
[Test file #103 in provided repository](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/103.html.test) 

[Test file #439 in provided repository](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/439.html.test) 


## For each test:
### Test 103:
-The implementation on local is correct, since it was able to give an output.

Actual Output:


<img width="202" alt="Screen Shot 2022-06-05 at 10 03 11 PM" src="https://user-images.githubusercontent.com/98505287/172097988-70ecb241-331c-498e-a3a7-1ea3a3364bcf.png">

Expected Output:


<img width="645" alt="Screen Shot 2022-06-05 at 9 59 37 PM" src="https://user-images.githubusercontent.com/98505287/172097697-2c3f1775-a889-47a6-b323-395f91505130.png">
There are no links as an expected output. --> []

### Test 439:
-The implementation in the markdown parser repository on my ieng6 account was correct.


Actual Output:


<img width="208" alt="Screen Shot 2022-06-05 at 10 04 56 PM" src="https://user-images.githubusercontent.com/98505287/172098151-437e8d7d-6c9c-4d0f-b98d-20f87d69e831.png">

Expected Output:


<img width="339" alt="Screen Shot 2022-06-05 at 10 06 15 PM" src="https://user-images.githubusercontent.com/98505287/172098251-00a6cfe4-a72e-4d63-85cc-b13849d152fc.png">

There are no links as an expected output. --> []

## Changes to the implementation:
For the implementation in test #103, I noticed there is a bug in the code since it causes an infinite loop to occur as well as improper finding of the links in the test cases. Although this test case does not contain any links, the fix to the code would involve having to make more if statements that provide a break to the loop below the highlighted code in the screenshot where it continues the loop. When it comes to having a test case with multiple characters like ", <,>,', etc there would need to be a piece of code that would determine that it is not a link if it has improper structure or if it has characters that are hindering the structure. The code needs to take in account characters while continuing to keep track of brackets, braces, code blocks and indices.


<img width="578" alt="Screen Shot 2022-06-05 at 10 22 26 PM" src="https://user-images.githubusercontent.com/98505287/172099850-01b78955-c1f1-4170-a3e7-2323460c2d15.png">




[Return to my site's homepage :)](https://briifernandez.github.io/cse15l-lab-reports/index.html) 

