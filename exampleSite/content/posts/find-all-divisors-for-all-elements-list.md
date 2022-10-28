---
title: "For each element in a list, Find count of divisors present in the list."
date: 2021-03-21T03:04:12+05:30
description: "Given a list of integers, find count of divisors present in the list. The number is divisor of itself. The list may contain duplicates. This solution solves the problem in n(log(n)) as compared to straight n^2."
tags: [tools]
---

I was working on a project involving multiple python files and many functions. Once I finished my projects with all the experimentation and edge cases, I was stuck with multiple lines of code with irregular formatting. Spent a lot of time to format the code before I could submit it for the review. Went on to find some better solution to skip the manual labour.

One of the best and easiest tool I came across was BLACK. Black is a utility that can be used to generate well formatting for your python projects with smallest diffs possible.

Black is truely a lifesaver and takes just a single line to convert your complete project to a consistent google style python formatting. Note: It won't change variable names or logic of your code, but just make it consistent in terms of formatting.

To install black on your machine:

~~~ {.bash}
from collections import Counter, defaultdict

def divisor_count(list_given):

    # find maximum element in the list
    max_n = max(list_given)

    # find frequencies
    freq = Counter(list_given)
    out = defaultdict(int)
 
    for i in freq:
      for j in range(i, max_n + 1, i):
        if j in freq:
          out[j] += freq[i]

    return max(out.values()), out

arr = [2, 8, 2, 5, 6, 10, 3]
max_divisor_count, divisor_count_map = divisor_count(arr)
print(f"Maximum number of divisors for a number in the list: {max_divisor_count}")
print(f"Divisor map: {divisor_count_map}")
~~~

Output is as follows:
~~~ {.bash}
Maximum number of divisors for a number in the list: 4
Divisor map: defaultdict(<class 'int'>, {2: 2, 6: 4, 8: 3, 10: 4, 5: 1, 3: 1})
~~~
![Black Before & After](https://github.com/abhishekbamotra/abhib/blob/master/exampleSite/content/posts/images/black_before_after.png?raw=true)
