# **Shortcuts: Streamlining and Simplifying Your Work**
---
This page is dedicated to displaying a variety of tips for simplifying work, especially as it relates to using Github's tools and servers. 
It focuses on three main sections:

## **Streamline SSH Configuration**
---
![First Code Change](https://alainajj.github.io/cse15l-lab-reports/FirstCodeChange.png)

[First Failure Inducing Input (Link)](https://github.com/AlainaJJ/markdown-parser/blob/main/test-file.md)

![First Code Symptom](https://alainajj.github.io/cse15l-lab-reports/FirstCodeSymptom.png)

The first bug I encountered when working on the MarkdownParse file was that an extra line at the end of the file would lead to an infinite loop, 
which would only be stopped by the memory being capped (which can be seen in the failure inducing input having an extra empty line at the end).
The bug led to the code searching for more links in the test-file.md, and since it didn't have any more links to find, it would search endlessly. 
I solved this bug by adding a code that checked for the currentIndex of an open bracket as being -1, indicating that no further line/link would be found.

## **Setup Github Access from ieng6**
---

## **Copy Whole Directories with 'scp-r'**
---
