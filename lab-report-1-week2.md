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
[VS Main Page](https://alainajj.github.io/cse15l-lab-reports/VSMainPage.png)
This page signifies that you have donwloaded the IDE successfully. You can move on to the next step!

## **Remotely Connecting**
---
For this step there will be three requirements:
1. Install OpenSSH using the guide found at [Open SSH Instructions](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)
2. Look up your course specific account, starting with 'cse15lsp', which is found over at [UCSD Student Accounts](https://sdacs.ucsd.edu/~icc/index.php)
3. Open the terminal on VS Studio Code and type your course specific account 'cse15lsp###@ieng6.ucsd.edu' as well as your password (if this is your first time logging in you'll have to select yes when prompted for '(yes/no/fingerprint)')

Once you go through all of these steps you should end up with something like this in the [VS Studio Code Terminal](https://alainajj.github.io/cse15l-lab-reports/RemoteConnectionStart.png)

## **Trying Some Commands**
---
Now to try some useful commands! A list of various commands that can be used in the terminal are:
* **cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/**,  and  
* **cat home/linux/ieng6/cs15lsp22/public/hello.txt** returns permission denied, represents that the 		user doesn’t have access 
* **mkdir new** makes a brand new directory called ‘new’
* **ls** shows the directories available
* **ls -a** represents more of the available directories
* **ls -lat** shows all of the directories and the time at which they were accessed or created

The below image displays these commands in use: [SSH Commands](https://alainajj.github.io/cse15l-lab-reports/CommandsSSH.png)


## **Moving Files with 'scp'**
---

## **Setting an SSH Key**
---

## **Optimizing Remote Running**
---

