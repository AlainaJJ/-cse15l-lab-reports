# **Test Galore: VimDiff, MarkdownParse, and Running Hundreds of Tests at a Time**
---
The focus for this page is running hundreds of provided tests on implementations of MarkdownParse, and comparing the outputs as a means 
to identify what needs to be improved in the implementations of a MarkdownParse.
---
## **How to Identify the Tests with Different Results?**

The easiest way in which I could find to demonstrate the different test outcomes after running the file was using 'vimdiff'. To do this
I had to create two different 'results.txt' files, one with the expected/correct outputs of the markdown parse file (left side of the
image) and one from the provided implementation of the Markdown Parse from Lab 9. Calling 'vimdiff' on these two results files causes 
any differing outcomes to be highlighted.

With it, I found there to be a large variety of differences:

![VimDiff SS](https://alainajj.github.io/cse15l-lab-reports/VimDiffSS.png)

## **Understanding and Displaying the Outcome of Two Tests**

The link for the two tests that will be looked at are provided below:

[Link to Test #1 (498)](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/498.md)

[Link to Test #2 (504)](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/504.md)

And the actual outcome that was obtained using the provided MarkdownRepository can similarly be seen here:

![VimTestOutcomes](https://alainajj.github.io/cse15l-lab-reports/VimTestOutcomes.png)

Lastly, we can see the expected outcome from the website [CommonMark](https://spec.commonmark.org/dingus/):

![ExpectedOutcome](https://alainajj.github.io/cse15l-lab-reports/VimTestOutcomes.png)

From this we can see start to analyzing what the proper implementation for the MarkdownParse file is. 

## **Addressing the Bug and Possible Fixes**

![CodeToImprove](https://alainajj.github.io/cse15l-lab-reports/CodeToImprove.png)




















## **Streamline SSH Configuration**
---
In order to simplify the access to the server 'ieng6' we can make a 'Host name' which is used alongside the command 'ssh' in order
to save time in having to type the original username. To do this a new file has to be set up under '~/.ssh' in your files, called 'config'
In this file you write the following:

![ShowConfig](https://alainajj.github.io/cse15l-lab-reports/ShowSSH1.png)

I personally created and modified this file in VS Code in a random folder and then moved it to the proper location with the 'mv' command:

![ShowConfig2](https://alainajj.github.io/cse15l-lab-reports/ShowSSH2.png)

Afterwards you can see the log-in working successfully with the new username provided 'cs15l':

![Successful Log In](https://alainajj.github.io/cse15l-lab-reports/ShowLogIn.png)

Lastly, the new username is seen in use when secure copying from the local computer to the server:

![Showing SCP](https://alainajj.github.io/cse15l-lab-reports/ShowSCP.png)

## **Setup Github Access from ieng6**
---
Due to current updates trying to commit and push to Github from an IDE often results to an error. You would usually be prompted for a 
username and password, but these are invalid ever since 2021. In order to solve this you can generate a brand new key in your ieng6
account and store it in Github, in order to gain access.

Here is a representation of where the key is stored in Github:

![Public Key Store](https://alainajj.github.io/cse15l-lab-reports/PublicKeyStore.png)

We can also see where the keys are stored within you server and account below (these were generated with 'ssh-keygen'). The public key 
is represented by id_rsa.pub, and the private key is id_rsa.

![Public and Private Key Store](https://alainajj.github.io/cse15l-lab-reports/PrivAndPubKey.png)

Now, we can once again run git commands such as 'commit' and 'push'

![Running Git Commands](https://alainajj.github.io/cse15l-lab-reports/ShowRunGit.png)

and the resulting commit can be seen in the link below.

[Resulting Commit](https://github.com/AlainaJJ/markdown-parser/commit/cfcb37b8ec23854e1468c3b912cca414b745cda6)

## **Copy Whole Directories with 'scp -r'**
---
Copying file by file can be a tedious task that can cost you a lot of time when working on projects. This can luckily be fixed with a simple
command, 'scp -r'. This command copies whole repositories, their folders, directories, and files, from your local computer to a server. To
use it you have to type 'scp -r' followed by the location you want to copy the directories and files to. 

![Copying Markdown-Parser](https://alainajj.github.io/cse15l-lab-reports/ShowCopyingFolder.png)

We can see this change by logging into the server and looking at 'markdown-parser'.

![Show Logging After Copy](https://alainajj.github.io/cse15l-lab-reports/ShowLogInCopy.png)

You can also simplify this process and even run files in a single line by combining different commands with ';'.

![Show Combination 1](https://alainajj.github.io/cse15l-lab-reports/ShowCom1.png)
![Show Combination 2](https://alainajj.github.io/cse15l-lab-reports/ShowCom2.png)
