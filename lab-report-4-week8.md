# **Creating (More) Tests for MarkdownParse**
---
In this page, several markdown parse tests will be created and their outputs will be demonstrated for both my code, and the code of 
another person's (a reviewed) repository.
---
## **Links to Repositories**
---
**Link to**
[Personal Repository](https://github.com/AlainaJJ/good-markdown-parser)

**Link to**
[Reviewed Repository](https://github.com/AlainaJJ/reviewed-markdown-parser)

## **Snippet #1: What Outcome do we Expect and Demonstrating the Tests Created**
---
**Expected Outcome**

Snippet 1-
google.com

(Based on the markdown parse website: [CommonMark](https://spec.commonmark.org/dingus/)

**Tests Created**

Personal-
![Personal MDP Tests](https://alainajj.github.io/cse15l-lab-reports/PersonalTestsSnip1.png)

Reviwed-
![Reviewed MDP Tests](https://alainajj.github.io/cse15l-lab-reports/ReviewedTestsSnip1.png)


## **Snippet #1: Actual Outcome on MarkdownParser**
---
Snip #1 failed the test for both me and the reviewed repository. The expected outcome
doesn't match the actual outcome, and the test appears as failing when run.
This can be seen in the below images:

My Markdown Parse-

![Personal MDP Outcome](ttps://alainajj.github.io/cse15l-lab-reports/GoodMarkdownTestOutputSnip1.png)

Forked Markdown Parse- 

![Reviewed MDP Outcome](ttps://alainajj.github.io/cse15l-lab-reports/ReviewedTestOutputSnip1.png)

## **Snippet #1: Possible Fixes for Failing Tests**
---
Inline Code w/ Backticks

---


## **Snippet #2: What Outcome do we Expect and Demonstrating the Tests Created**
---
**Expected Outcome**

Snippet 2-
a.com
a.com(())
example.com

(Based on the markdown parse website: [CommonMark](https://spec.commonmark.org/dingus/)

**Tests Created**

Personal-
![Personal MDP Tests](https://alainajj.github.io/cse15l-lab-reports/PersonalTestsSnip2.png)

Reviwed-
![Reviewed MDP Tests](https://alainajj.github.io/cse15l-lab-reports/ReviewedTestsSnip2.png)

## **Snippet #2: Actual Outcome on MarkdownParser**
---
Snip #2 failed the test for both me and the reviewed repository. The expected outcome
doesn't match the actual outcome, and the test appears as failing when run.
This can be seen in the below images:

My Markdown Parse-

![Personal MDP Outcome](ttps://alainajj.github.io/cse15l-lab-reports/GoodMarkdownTestOutputSnip1.png)

Forked Markdown Parse- 

![Reviewed MDP Outcome](ttps://alainajj.github.io/cse15l-lab-reports/ReviewedTestOutputSnip1.png)

## **Snippet #2: Possible Fixes for Failing Tests**
---
Nested Parentheses, Brackets, and Escaped Brackets

---


## **Snippet #3: What Outcome do we Expect and Demonstrating the Tests Created**
---
**Expected Outcome**

Snippet 3-
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule

(Based on the markdown parse website: [CommonMark](https://spec.commonmark.org/dingus/)

**Tests Created**

Personal-
[Personal MDP Tests](https://alainajj.github.io/cse15l-lab-reports/PersonalTestsSnip3.png)

Reviwed-
[Reviewed MDP Tests](https://alainajj.github.io/cse15l-lab-reports/ReviewedTestsSnip3.png)

## **Snippet #3: Actual Outcome on MarkdownParser**
---
Snip #3 failed the test for both me and the reviewed repository. The expected outcome
doesn't match the actual outcome, and the test appears as failing when run.
This can be seen in the below images:

My Markdown Parse-

![Personal MDP Outcome](ttps://alainajj.github.io/cse15l-lab-reports/GoodMarkdownTestOutputSnip1.png)

Forked Markdown Parse- 

![Reviewed MDP Outcome](ttps://alainajj.github.io/cse15l-lab-reports/ReviewedTestOutputSnip1.png)


## **Snippet #3: Possible Fixes for Failing Tests**
---
Newlines in Brackets

