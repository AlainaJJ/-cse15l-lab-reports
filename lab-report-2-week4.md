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

## **Change Number 2: Images Considered as Links**
---

![Second Code Change](https://alainajj.github.io/cse15l-lab-reports/SecondCodeChange.png)

[Second Failure Inducing Input (Link)](https://github.com/AlainaJJ/markdown-parser/blob/main/image-test.md)

![Second Code Symptom](https://alainajj.github.io/cse15l-lab-reports/SecondCodeSymptom.png)

The second bug that I dealt with was the file mistakenly adding images as links to the list. It would incorrectly misinterpret the contents inside 
of the parentheses for a link due to the similar syntax of images and links. The failure inducing input was the use of images 
("![]" instead of just "[]") and the symptom would be the images being added to the list of links. This problem was solved by ensuring that the code 
only added the contents within the parentheses, if an exclamation didn't precede the opening bracket (i.e.- only if "!" wasn't present before "[" ).

## **Change Number 3: Missing Parentheses**
---

![Third Code Change](https://alainajj.github.io/cse15l-lab-reports/ThirdCodeChange.png)
*Image cropped to display specific area that was altered

[Third Failure Inducing Input (Link)](https://github.com/AlainaJJ/markdown-parser/blob/main/missing-paren.md)

![Third Code Symptom](https://alainajj.github.io/cse15l-lab-reports/ThirdCodeSymptom.png)

The third and final bug I dealt with happened when a line was missing either an open or close parentheses. To test this I used a variety of 
test files, however, the final one I ended up with, and the one demonstrated as the failure inducing input has an actual link, a missing opening
parenthesis, and a missing closing parenthesis. The symptom of the bug would be an improper set of links being returned in the list, as the program
could not differentiate when it was supposed to stop looking for the content inside the parenthesis. I solved this by simply looking for a missing
parenthesis before the declaration of the parenthesis variable index. It would make sure there was a closing or opening parenthesis and would 
otherwise 'break'.


