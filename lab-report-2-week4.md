# **Markdown Parse Code Improvement**
---
The Markdown Parse code was bad, so I fixed it... kinda.

## **Change Number 1: Extra Empty Line at the End of the File**
---
![First Code Change](https://alainajj.github.io/cse15l-lab-reports/FirstCodeChange.png)

[First Failure Inducing Input (Link)](https://github.com/AlainaJJ/markdown-parser/blob/main/test-file.md)

![First Code Symptom](https://alainajj.github.io/cse15l-lab-reports/FirstCodeSymptom.png)

The first bug in encountered when working on the MarkdownParse file was that an extra line at the end of the file would lead to an infinite loop, 
which would only be stopped by the memory being capped (which can be seen in the failure inducing input having an extra empty line at the end).
The bug led to the code searching for more links in the test-file.md, and since it didn't have any more links to find, it would search endlessly. 
I solved this bug by adding a code that checked for the currentIndex of an open bracket as being -1, indicating that no further line/link would be found.

## **Change Number 2: **
---

![Second Code Change](https://alainajj.github.io/cse15l-lab-reports/SecondCodeChange.png)

[Second Failure Inducing Input (Link)](https://github.com/AlainaJJ/markdown-parser/blob/main/image-test.md)

![Second Code Symptom](https://alainajj.github.io/cse15l-lab-reports/SecondCodeSymptom.png)

The second bug that I dealt with was the file mistakenly adding images as links to the list. It would incorrectly misinterpret the contents inside 
of the parentheses for a link due to the similar syntax of images and links. The failure inducing input was the use of images 
('![]()' instead of just '[]()') and the symptom would be the images being added to the list of links. This problem was solved by ensuring that the code 
only added the contents within the parentheses, if an exclamation didn't precede the opening bracket (i.e.- only if '!' wasn't present before '[' ).

