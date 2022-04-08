# **Tutorial: How to Log into Course-Specific Account on 'ieng6'**
---
Logging into your course specific account can be a difficult and confusing task, but this guide is here to help make it simple!

## **Installing VS Code**
---
First, you want to download the IDE Visual Studio Code. If you already have Visual Studio Code downloaded feel free to skip this part. Otherwise, the program can be downloaded by accessing the website:
[Visual Studio Code Website](https://code.visualstudio.com/)
![VS Download Page](https://alainajj.github.io/cse15l-lab-reports/VSDownload.png)
Once you're on this page select download for the particular software you're using.

After you've downloaded and opened VS Studio Code you should see something like this:
![VS Main Page](https://alainajj.github.io/cse15l-lab-reports/VSMainPage.png)
This page signifies that you have donwloaded the IDE successfully. You can move on to the next step!

## **Remotely Connecting**
---
For this step there will be three requirements:
1. Install OpenSSH using the guide found at [Open SSH Instructions](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)
2. Look up your course specific account, starting with 'cse15lsp', which is found over at [UCSD Student Accounts](https://sdacs.ucsd.edu/~icc/index.php)
3. Open the terminal on VS Studio Code and type your course specific account 'cse15lsp###@ieng6.ucsd.edu' as well as your password (if this is your first time logging in you'll have to select yes when prompted for '(yes/no/fingerprint)')

Once you go through all of these steps you should end up with something like this in the ![VS Studio Code Terminal](https://alainajj.github.io/cse15l-lab-reports/RemoteConnectionStart.png)

## **Trying Some Commands**
---
Now to try some useful commands! A list of various commands that can be used in the terminal are:
* **cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/**,  and  
* **cat home/linux/ieng6/cs15lsp22/public/hello.txt** returns permission denied, represents that the 		user doesn’t have access 
* **mkdir new** makes a brand new directory called ‘new’
* **ls** shows the directories available
* **ls -a** represents more of the available directories
* **ls -lat** shows all of the directories and the time at which they were accessed or created

The below image displays these commands in use: ![SSH Commands](https://alainajj.github.io/cse15l-lab-reports/CommandsSSH.png)


## **Moving Files with 'scp'**
---
In this section we will cover 'scp' (otherwise known as secure copy). Secure copy is a command that can be used to make a copy, usually between the client (you the user and your files) and the server (the thing you've been struggling to connect to for the last 15 minutes). 

The way scp works is 'scp (file name) (location where you want the file to be copied)'

This is best seen in the image below where the file *WhereAmI.java* is compiled, ran, and then scp'd from the client to the server:
![SCP WhereAmI.java](https://alainajj.github.io/cse15l-lab-reports/SCPJava.png)

## **Setting an SSH Key**
---
At this point a frequent problem that you face with wanting to access the server and run the 'scp' command is that you're required to enter your password everytime. This can actually be overcome with something known as an 'ssh key'. An 'ssh key' is used to created public and private keys which you can save in your server directory, to avoid having to type your password everytime. 

To do this type the command 'ssh-keygen' in the VS Studio Code terminal. This creates a copy of the public key on the server, and the private key in the client. When using the command 'ssh-keygen' you will be asked to enter a passphrase, but you can just press enter to avoid having to type in any passphrase at all.

Following this step you will end up wtih two files 'id_rsa' and 'id_rsa.pub', representing the private and public keys respectively. In order to make sure the SSH key works as intended you have to copy the public (id_rsa.pub) key to the ssh directory (cs15lsp22###@ieng6.ucsd.edu)
![SSH Key Copy](https://alainajj.github.io/cse15l-lab-reports/SSHKeyFirst.png)

Once this step is completed you should be able to log into the SSH without having to type your school password 
![SSH Key](https://alainajj.github.io/cse15l-lab-reports/SSHKey.png)

## **Optimizing Remote Running**
---
Lastly, we will address ways in which you can make this entire process significantly shorter. Some things to note are:
* when we run 'ssh' we can also call a command afterward like this: 'ssh cs15lsp22###@ieng5.ucsd.edu ls'
* we can use semicolons to run multiple commands at the same time: 'cp WhereAmI.java; javac WhereAmI.java; java WhereAmI'
* we can copy paste large segments of code to avoid having to type them out (like the ssh course specific account)

Using this knowledge we can show an example of compiling and running a file that was just changed from the client, on the server ![Optimized Running](https://alainajj.github.io/cse15l-lab-reports/Optim.png)

We can see that the above code was run in a single line in the ssh server (65 keystrokes if you typed it all out, or a measly 8 if you're lazy like me and copy pasted both the ssh and the compile and run commands)
