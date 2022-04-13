# Remote Access (Week 2 Lab Report)

## Installing VScode
<img width="570" alt="Screen Shot 2022-04-07 at 4 33 03 PM" src="https://user-images.githubusercontent.com/98505287/162337665-d6ac1ac0-a831-46a8-bd89-edaa755d63df.png">
1. First, I downloaded VScode from their website and opened the application on my computer with my own account.
2. By logging in and using my personal computer, I would have access to all of my folders and files that can be accessed by selecting File --> Open Folder/File.
3. I have set the auto-save option on my account which is helpful in keeping my edits updated on my account.

## Remotely Connecting
<img width="570" alt="Screen Shot 2022-03-31 at 4 17 41 PM" src="https://user-images.githubusercontent.com/98505287/162337698-94194a55-9398-48d6-9a2f-e86eaa2807d6.png">
1. To remotely connect to the remote server, I would have to create a new terminal and type `ssh cs15lsp22asy@ieng6.ucsd.edu` onto the command line which would then cause a **password message** to pop up.
2. After entering the password, I would have access to my own personal directories on the remote server.

## Trying Some Commands
<img width="570" alt="Screen Shot 2022-04-07 at 4 40 36 PM" src="https://user-images.githubusercontent.com/98505287/162337720-6de440da-070c-43e7-86a1-0297fe5fe74e.png">
1. Commands can be done on our desktop and after ssh to the remote server.
2. Commands allow us to view certain details about the account (even *hidden* details!), the commands that will be useful include: `ls(list files), ls -l(longer format of list), ls -a(hidden files), cd /(root directory), cd(home directory), cd ..(previous directory), pwd(working directory), cat filename(display contents of file), javac file; java fileclass(compile and run), and cp filetocopy filedestination(copies contents of file1 to file destination)`.
3. Another helpful tip with runtime would be to combine the commands with **";"** which would run all your commands all at once!

## Moving Files with scp
<img width="570" alt="Screen Shot 2022-04-07 at 4 44 31 PM" src="https://user-images.githubusercontent.com/98505287/162337760-7ba49ef8-0a3b-4219-9c7c-2ba696daa859.png">
1. By updating a local file, in order to save changes onto the remote server we would have to use `scp WhereAmI.java cs15lsp22asy@ieng6.ucsd.edu:~/` on our desktop terminal.
2. Then, by `ssh cs15lsp22asy@ieng6.ucsd.edu`, we can `ls` to see if the file is in the home directory and `cat WhereAmI.java` can display the contents of the file.
3. To move a file into a new directory, we can `mkdir NewDirectory` and `mv WhereAmI.java NewDirectory`. Then, we can `cd NewDirectory` and `ls` to view the files in that directory. 


## Setting an SSH Key
<img width="570" alt="Screen Shot 2022-04-07 at 4 45 56 PM" src="https://user-images.githubusercontent.com/98505287/162337790-b8df3e29-5940-4da2-8c8f-08a3306160da.png">
1. On our desktop, create new terminal and type `ssh-keygen` which would create a public and private key. We would have to select the file to place key `(/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa`. Once asked to enter passphrase, press *enter*. 
2. A key fingerprint should appear and we need to `ssh cs15lsp22asy@ieng6.ucsd.edu`, `mkdir .ssh`, then exit.
3. We need to move the public key through `$ scp /Users/<user-name>/.ssh/id_rsa.pub
cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys`. Now we are able to ssh **without** a password!


## Optimizing Remote Running
<img width="570" alt="Screen Shot 2022-04-07 at 4 54 27 PM" src="https://user-images.githubusercontent.com/98505287/162337795-2a668b34-c4c6-4576-8275-8ff5541f85ba.png">
1. Remote Running can be done in *ease* by having certain commands combined by using `;` in between each command. 
2. By setting an SSH key we are able to login without a password and utilizing the up-arrow for previous commands can make the proccess more efficient!


[Link to my site :)](https://briifernandez.github.io/cse15l-lab-reports/index.html) 
