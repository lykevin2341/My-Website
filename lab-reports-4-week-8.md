[Back to main page](https://lykevin2341.github.io/cse15l-lab-reports/index.html)

[Back to lab reports](https://lykevin2341.github.io/cse15l-lab-reports/LabReports.html)

# Lab Report 4 - Snippet Tests

## MarkdownParse Tests Written
> These are the tests that I wrote for the three snippets. These are the same tests in my markdown parse and the markdown parse that I reviewed. It show cases the expected values, and asserts whether my current markdown's output equals the expected.

![image](/Lab4Images/snippet%20tests.png)

## My MarkdownParse Output

![image](/Lab4Images/my%20tests.png)
> I passed test 1 but not 2 or 3

## The MarkdownParse I Reviewed's Output

![image](/Lab4Images/reviewed%20tests.png)
> None of the tests passed


# Possible Fixes to MarkdownParse
## Snippet 1
I passed this specific test with snippit 1, but I am uncertain if it would pass with all tests that have backticks. It is possible I had the incorrect expected value, if that is the case, I should add a line that accounts for specifically back ticks in my markdown parse. (I genuinely don't know why my test passes)

## Snippet 2
I think a possible code fix could be some type of code counter to keep track of whether the parenthesis is inside of a brace or not, and then have an if statement that would see if it is a nested parenthesis and work accordingly.

## Snippet 3
The issue with this test is that the end parenthesis comes after another link was put inside, and the program gets confused. A possible fix is to check for a closed parenthesis before a new link line to see if the link was actually finished and closed, and if it isn't it would make the new link line put in valid.