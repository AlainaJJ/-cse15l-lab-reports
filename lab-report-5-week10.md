# **Test Galore: VimDiff, MarkdownParse, and Running Hundreds of Tests at a Time**
---
The focus for this page is running hundreds of provided tests on implementations of MarkdownParse, and comparing the outputs as a means 
to identify what needs to be improved in the implementations of a MarkdownParse.

---
## **How to Identify the Tests with Different Results?**

The easiest way in which I could find to demonstrate the different test outcomes after running the file was using 'vimdiff'. To do this
I had to create two different 'results.txt' files, one with the expected/correct outputs of the markdown parse file (left side of the
image) and one from my implementation of the MarkdownParse file. Calling 'vimdiff' on these two results files causes any differing outcomes 
to be highlighted.

With it, I found there to be a large variety of differences:

![VimDiff SS](https://alainajj.github.io/cse15l-lab-reports/VimDiffSS.png)

## **Understanding and Displaying the Outcome of Two Tests**

The link for the two tests that will be looked at are provided below:

[Link to Test #1 (498)](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/498.md)

[Link to Test #2 (504)](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/504.md)

And the actual outcomes that were obtained by my MarkdownParse can similarly be seen here:

![VimTestOutcomes](https://alainajj.github.io/cse15l-lab-reports/VimTestOutcomes.png)

Lastly, we can see the expected outcome from the website [CommonMark](https://spec.commonmark.org/dingus/):

![ExpectedOutcome](https://alainajj.github.io/cse15l-lab-reports/ExpectedOutcomes.png)

From this we can note that the proper implementation of the file is the one seen by CommonMark which has a single url for test 498,
and 3 urls for 504.

## **Addressing the Bug and Possible Fixes**

Having seen the expected outcomes we can start analyzing what changes are necessary to improve my copy of MarkdownParse. The main
error can be seen in the picture below. 

![CodeToImprove](https://alainajj.github.io/cse15l-lab-reports/CodeToImprove1.png)

The problem with this line of code is that it breaks to the return statement if the open bracket is greater than the ending 
brackets or parentheses. This is why the actual result of the test on my markdown parser is an emtpy array. One way to fix this
is to no longer break if there are "parentheses or closing brackets" out of order, and to ensure that there are that the 
file keeps track of the number and position of parentheses encountered, so as to know when the link actually ends, and not get
tripped up by the nested parentheses. 
