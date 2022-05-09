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
To store a public key on GitHub, I would have to copy the contents of the public key by using the command `pbcopy < ~/.ssh/id_rsa.pub`. I would press New SSH key, then paste the contents over and include the name as Personal Macbook. 

<img width="970" alt="Screen Shot 2022-05-07 at 10 51 43 PM" src="https://user-images.githubusercontent.com/98505287/167283786-df5ba76d-6c6c-4e1c-8e1b-06dce31a73ef.png">



**public key stored on user account:**
The public key is the file `id_rsa.pub`, and it was `scp` into the user account. I used `mv id_rsa.pub .ssh` to move the file into the .ssh directory.

<img width="448" alt="Screen Shot 2022-05-07 at 10 55 18 PM" src="https://user-images.githubusercontent.com/98505287/167283822-cf3fac8c-1afa-4cd3-9fcd-8395de13c461.png">

**private key stored on user account:**
The private key is the file `id_rsa`, and it was `scp` into the user account. I used `mv id_rsa .ssh` to move the file into the .ssh directory.

<img width="448" alt="Screen Shot 2022-05-07 at 10 55 18 PM" src="https://user-images.githubusercontent.com/98505287/167283837-1c6d0706-5cfe-45f8-ab03-0cb1bb326274.png">

*Side Note:* I also created a `config` file in the .ssh directory. It contains the Host, HostName, User, and IdentityFile which is similar to the `config` file that is on my local machine. 

*Personal Token:* After cloning a repository onto the user account, I had to generate a personal token on GitHub in order to have the ability to commit and push. I copied the token and used the command `git remote set-url origin https://<token>@github.com/<username>/<repo>` which configures the personal token.

`git` **commands in ieng6 account:**
Firstly, to pull updates to the repository I used `git pull`. Then, I used `vim <filename>` to update any changes I would like to make to the file. Afterwards, I moved the file to the staging area by using `git add <filename>`. When the file is ready to be commited, I used the command `git commit -a -m "<commit message>"` which commits the file and avoids the commit message. Final step is to `git push` and a message should appear!

<img width="656" alt="Screen Shot 2022-05-07 at 10 59 26 PM" src="https://user-images.githubusercontent.com/98505287/167283943-f87c3edc-1048-4998-88f6-15b9a37ba609.png">

**Link to commit:**

[Commit Made on User Account](https://github.com/briifernandez/markdown-parser/commit/05e7d3980c316092a34a139b42d68f3d5f011ab3)


---
## Copy Whole Directories with `scp -r`
**Copying markdownparse directory into ieng6 account:**
To 
<img width="738" alt="Screen Shot 2022-05-08 at 10 04 35 PM" src="https://user-images.githubusercontent.com/98505287/167344643-c6dfca1d-a014-4c1e-aab6-7ccc75bd038b.png">


**Logging in and compiling (also combining commands with `;` ):**

<img width="952" alt="Screen Shot 2022-05-08 at 10 05 45 PM" src="https://user-images.githubusercontent.com/98505287/167344544-6dfb318c-51db-4f5f-950e-6c5905b77c9f.png">
<img width="958" alt="Screen Shot 2022-05-08 at 10 16 42 PM" src="https://user-images.githubusercontent.com/98505287/167345080-9d35bbe7-42ea-4e05-bf31-2aa5be8254d7.png">





[Return to my site's homepage :)](https://briifernandez.github.io/cse15l-lab-reports/index.html) 
