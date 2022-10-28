---
title: "For each element in a list, Find count of divisors present in the list."
date: 2022-10-27T09:00:42+05:30
description: "Given a list of integers, find count of divisors present in the list. The number is divisor of itself. The list may contain duplicates. This solution solves the problem in n(log(n)) as compared to straight n^2."
tags: [coding]
---

Given a list of integers, find count of divisors present in the list. The number is divisor of itself. The list may contain duplicates. Each element is equal to or greater than 1. Elements in the list can be in any order.


This solution solves the problem in n(log(m)) where m is the max element as compared to straight n^2.

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
