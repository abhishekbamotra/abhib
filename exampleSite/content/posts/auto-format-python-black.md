---
title: "Auto format your python code - Black"
date: 2021-03-21T03:04:12+05:30
description: "Black is a utility that can be used to generate well formatting for your python projects with smallest diffs possible."
tags: [tools]
---

I was working on a project involving multiple python files and many functions. Once I finished my projects with all the experimentation and edge cases, I was stuck with multiple lines of code with irregular formatting. Spent a lot of time to format the code before I could submit it for the review. Went on to find some better solution to skip the manual labour.

One of the best and easiest tool I came across was BLACK. Black is a utility that can be used to generate well formatting for your python projects with smallest diffs possible.

Black is truely a lifesaver and takes just a single line to convert your complete project to a consistent google style python formatting. Note: It won't change variable names or logic of your code, but just make it consistent in terms of formatting.

To install black on your machine:

~~~ {.bash}
pip install black
~~~

Go to the project you want to format.

~~~ {.bash}
black -l120 .
~~~

-l is an option to choose the line length in the example above it is 120 characters. Dot (.) at the end is used to choose the directory or file which you want to format. If you want to format all the files in current directory, just write dot else a directory or file path.

Command for one file formatting is:

~~~ {.bash}
black -l120 example_path/example_python_file.py
~~~

Example of before and after formatting.

![Black Before & After](/images/black_before_after.png)