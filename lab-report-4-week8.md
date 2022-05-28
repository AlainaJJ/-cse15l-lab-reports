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

(Based on the markdown parse website: [CommonMark](https://spec.commonmark.org/dingus/))

**Tests Created**

Personal-
![Personal Snip Test 1](https://alainajj.github.io/cse15l-lab-reports/PersonalTestsSnip1.png)

Reviwed-
![Reviewed Snip Test 1](https://alainajj.github.io/cse15l-lab-reports/ReviewedTestsSnip1.png)

## **Snippet #1: Actual Outcome on MarkdownParser**
---

Snip #1 failed the test for both me and the reviewed repository. The expected outcome
doesn't match the actual outcome, and the test appears as failing when run.
This can be seen in the below images:

My Markdown Parse-

![Personal MDP Outcome 1](https://alainajj.github.io/cse15l-lab-reports/GoodMarkdownTestOutputSnip1.png)

Reviewed Markdown Parse- 

![Reviewed MDP Outcome 1](https://alainajj.github.io/cse15l-lab-reports/ReviewedTestOutputSnip1.png)

## **Snippet #1: Possible Fixes for Failing Tests**
---

*Inline Code w/ Backticks*

Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases 
that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

*Answer:*

Yes. I can see a code that exists within 10 lines that ensures that backticks are assessed properly in our markdown parse file.
It would check for the symbol and indexOf the backticks (') and would keep track of their position based on the aforementioned
indexOf value to ensure that the link is either displayed, or not. It might take closer to 10 lines, but I do consider it
doable. It might have to be incorporated across different parts of the MarkdownParse file, (start and in return statements), but
would still exist within the max line limit.

---


## **Snippet #2: What Outcome do we Expect and Demonstrating the Tests Created**
---

**Expected Outcome**

Snippet 2-
a.com
a.com(())
example.com

(Based on the markdown parse website: [CommonMark](https://spec.commonmark.org/dingus/))

**Tests Created**

Personal-
![Personal Snip Test 2](https://alainajj.github.io/cse15l-lab-reports/PersonalTestsSnip2.png)

Reviwed-
![Reviewed Snip Test 2](https://alainajj.github.io/cse15l-lab-reports/ReviewedTestsSnip2.png)

## **Snippet #2: Actual Outcome on MarkdownParser**
---

Snip #2 failed the test for both me and the reviewed repository. The expected outcome
doesn't match the actual outcome, and the test appears as failing when run.
This can be seen in the below images:

My Markdown Parse-

![Personal MDP Outcome 2](https://alainajj.github.io/cse15l-lab-reports/GoodMarkdownTestOutputSnip2.png)

Reviewed Markdown Parse- 

![Reviewed MDP Outcome 2](https://alainajj.github.io/cse15l-lab-reports/ReviewedTestOutputSnip2.png)

## **Snippet #2: Possible Fixes for Failing Tests**
---

*Nested Parentheses, Brackets, and Escaped Brackets*

Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases 
that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be 
a more involved change.

*Answer:*

No. I think this is one of the snippet tests that would have a more involved case. In my opinion it would be slightly
more complicated to account for which parentheses and brackets should count for the link when they're all nested. I think the
change is still doable however. I could easily see something that checks where the first open bracket is, keeps track of 
the ending bracket, updating its indexOf every time a new one is encountered. The same would be done for the parentheses
to ensure that only 1 pair of brackets and parenthess (opening and closing) are used to identify what belongs within a link.
That being said the change might take more than a 10 lines, and might have to be incorporated across different parts of the
MarkdownParse file (next to currentIndex, before return statements, when declaring parentheses and brackets and etc.).

---


## **Snippet #3: What Outcome do we Expect and Demonstrating the Tests Created**
---

**Expected Outcome**

Snippet 3-
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule

(Based on the markdown parse website: [CommonMark](https://spec.commonmark.org/dingus/))

**Tests Created**

Personal-
![Personal MDP Snip Test 3](https://alainajj.github.io/cse15l-lab-reports/PersonalTestsSnip3.png)

Reviwed-
![Reviewed MDP Snip Test 3](https://alainajj.github.io/cse15l-lab-reports/ReviewedTestsSnip3.png)

## **Snippet #3: Actual Outcome on MarkdownParser**
---

Snip #3 failed the test for both me and the reviewed repository. The expected outcome
doesn't match the actual outcome, and the test appears as failing when run.
This can be seen in the below images:

My Markdown Parse-

![Personal MDP Outcome 3](https://alainajj.github.io/cse15l-lab-reports/GoodMarkdownTestOutputSnip3.png)

Reviewed Markdown Parse- 

![Reviewed MDP Outcome 3](https://alainajj.github.io/cse15l-lab-reports/ReviewedTestOutputSnip3.png)

## **Snippet #3: Possible Fixes for Failing Tests**
---

*Newlines in Brackets*

Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related 
cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would 
be a more involved change.

*Answer:*

Yes. I think the problem with snippet 3 could easily be resolved with a less than 10 lines fix. This is because
within the markdown parser files (both mine and reviewed) we are already checking for the index of unique characters such
as "!" to avoid confusing links for images. This same structure could be used, except this time to check for newlines within 
the brackets and parentheses instead. 
parentheses 
