[Back to main page](https://lykevin2341.github.io/cse15l-lab-reports/index.html)

[Back to lab reports](https://lykevin2341.github.io/cse15l-lab-reports/LabReports.html)

# Lab Report 3 - Streamlining GitHub in ieng6

## Streamling SSH Process
```
In this step, I will be making the ssh log in process more streamlined by using a chosen moniker for log in instead of the whole cs15lsp22zzz@ieng6.ucsd.edu username
```

>Screenshot of my .ssh/config file after adding in the new username used with my ssh keys

![image](Lab3Images/streamline%20ssh%20config%20file.png)


>Here is a screenshot of me logging into my ieng6 account using the new username I gave it.

![image](Lab3Images/ssh%20shortcut.png)


>Next I copied a file onto my ieng6 using `scp` and the new moniker I gave for logging in.

![image](Lab3Images/SCP%20with%20ieng6.png)


## Setup GitHub Access from ieng6

```
For this step I made it so that github commands such as "push" and "commit" can be done through ieng6
```

>This is a screenshot of my ssh key on my github keys page

![image](Lab3Images/ssh%20keys.png)

>This shows the location of my private ssh key. There are two, one for my ieng6 log in, and the other for using GitHub in ieng6

![images](Lab3Images/ssh%20key%20location.png)

>This nex screenshot shows me using the `git add` method to add a file to my repository. I then used the `git status` method to make sure that the change was documented. I then did `git commit` to commit the change with the description "Added test file". I then finished it by doing `git push origin main` to push the commit to the repository. This was all done while in my ieng6 account.

![images](Lab3Images/git%20push%20and%20commit.png)

[Link to the commit on GitHub](https://github.com/lykevin2341/markdown-parser/commit/08f9e6d9e8198e002b7a7fcb66dadbe3f17ad11a)

## Copy Whole Directories with `scp -r`

```
For this step, we are copying entire directories instead of singular files at a time using the command "scp -r"
```

>This step had a really long list of things getting copied over, but I split it into three screen shots to show the most important parts of it copying.

![image](Lab3Images/scp%20all%20file%201.png)
![image](Lab3Images/scp%20all%20file%202.png)
![image](Lab3Images/scp%20all%20file%203.png)

>This next step is me running and compiling my `MarkdownParseTest.java` file with `javac -cp .:lib\junit-4.13.2.jar:lib\hamcrest-core-1.3.jar MarkdownParseTest.java`, which for some reason has issues compiling when it works fine on my local computer. There is also a single failure when running the file using `java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest` This seems to have shown up after the latest lab and for some reason I can't fix it.

![image](Lab3Images/java%20compile%20and%20run%201.png)
![image](Lab3Images/java%20compile%20and%20run%202.png)

>This last step I try to scp, ssh, and run the tests in one single line