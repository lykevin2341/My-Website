# Lab Report 2: Debugging MarkdownParse

```
In this lab I will be showing some of the updates my partners and I made to the markdownparse code to debug issues.
```

## First: Extra Character Causing OutOfMemoryError

![image](Images/first%20update%20commit.png)

>Link to the failure inducing input file:
[Test File Link](https://github.com/dfeliton/markdown-parser/blob/main/different-test-file.md)

![image](Images/first%20update%20commit%20error%20output.png)

>The failure inducing input is the ";" added on to the end of one of the links being parsed, which leads to the computer running out of memory when trying to run the program. Possibly caused by some form of infinite loop because teh currentIndex is never updated to the proper size to end loop.

## Second: Invalid URL Formatting

![image](Images/Second%20update%20commit.png)

>Link to failure inducing input:
[Test File Link](https://github.com/dfeliton/markdown-parser/blob/main/test-file2.md)

![image](Images/Second%20update%20ommit%20error.png)

>The failure inducing input is the lack of "[]" for the link. Improper link formats causes an infinite loop error that causes the code to run out of memory in the java heap space.

## Third: Having No URL's or Valid URL's In Markdown File

![image](Images/Third%20update%20commit.png)
![image](Images/Third%20update%20commit%202.png)

>Link to failure inducing input:
[Test File Link](https://github.com/dfeliton/markdown-parser/blob/main/test-file3.md)

![image](Images/third%20update%20commit%20error.png)

>The the failure inducing input is having no URL's or invalid URL's in the markdown file. There is an bug in the code that doesn't account for any extra characters besides where the "[]" and "()" are expected to be, so it causes infinite loops. This prints proper errors to avoid these symptops of infinite loops.
