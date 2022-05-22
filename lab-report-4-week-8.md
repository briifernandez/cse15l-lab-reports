# Week 8 Lab Report 4 

## Repositories Used:
[My markdown-parse Repository](https://github.com/briifernandez/markdown-parser) 
[Week 7 Reviewed Repository](https://github.com/nathom/markdown-parser) 

## Expected Output for All Snippets:
<img width="488" alt="Screen Shot 2022-05-22 at 9 45 28 AM" src="https://user-images.githubusercontent.com/98505287/169706573-2c275533-23b1-44a2-8557-bfcb9b851db5.png">

## 3 Test Cases for my Implementation :
<img width="611" alt="Screen Shot 2022-05-22 at 9 54 55 AM" src="https://user-images.githubusercontent.com/98505287/169706643-03d96ed2-ee17-46c7-a3be-27c9ccef83a2.png">

## Tests that Failed:
<img width="934" alt="Screen Shot 2022-05-22 at 9 55 06 AM" src="https://user-images.githubusercontent.com/98505287/169706677-9c21ad76-5f79-4c23-8e23-cb94bb36a6aa.png">

## 3 Test Cases for Reviewed Implementation :

<img width="605" alt="Screen Shot 2022-05-22 at 10 06 25 AM" src="https://user-images.githubusercontent.com/98505287/169707032-061bfac1-f215-41b8-bd1f-e27c01136de4.png">


## Tests that Failed:

<img width="852" alt="Screen Shot 2022-05-22 at 10 07 07 AM" src="https://user-images.githubusercontent.com/98505287/169707059-be58b2a4-94a9-4579-9766-c9d070c7bbfa.png">


## Improvements to My Implementation:

1. In snippet one, the test case did not pass and I think there is a small code change that can allow my program to work. The code change would be to consider backticks and I need to create an if statement in my while loop that breaks the loop/ not consider the string a link if the backticks are outside of closeBracket, openBracket, or openParen.  Otherwise, the backticks inside the brackets or parentheses have been considered a link, and backticks outsie of closeParen still allowed the String to be a link.

2. For snippet two, the test case I wrote for my implementation had passed and it fixes the nest parentheses and brackets issue. The code change that allowed it to work was that the while loop had an if statement that addressed if openBracket, closeBracket, openParen, or closeParen were not present, the loop would have to break.

3. In snippet three, my test failed and I think there is a small code change that could make my program work. The code change would have to consider line breaks by continuing the loop until the next openBracket is detected or if text is detected, so it would determine where to stop looking for a closeParen.




[Return to my site's homepage :)](https://briifernandez.github.io/cse15l-lab-reports/index.html) 
