# Lab Report 5

Since I'm only looking for two code differences, I opted to manually find these two tests.
If I needed to record all differences, I likely would'ved used the `diff` command.

## Test 342
Here is test 342:

![Image](342md.png)

Here is the actual output:

![Image](342output.png)

Here is what my markdown-parse returns:

![Image](342mine.png)

Here is what the cloned markdown-parse returns:

![Image](342cloned.png)

As you can see both versions of markdown-parse are wrong.
Even though in reality there is no link, both still return a non-zero list. 
The change I can make to my own markdown parse is to implement a system that prioritizes ticks.
The system would check for a tick within a set of brackets and see if there was another tick with a greater index.
If so, the loop would jump the index to the tick with the larger index. 
Then, the program would continue searching for links.


## Test 516

Here is test 487:

![Image](487md.png)

Here is the actual output:

![Image](487output.png)

Here is what my markdown-parse returns:

![Image](487mine.png)

Here is what the cloned markdown-parse returns:

![Image](487cloned.png)

As you can see my mark-down failed this test case.
The content within the parenthesis isn't considered a link because it contains a space.
Therefore, the code change I would make is to first use the method `trim()` to remove white space at the beginning and end of the potential link.
Then, I would check for if there was a white space still within the potential link.
If there is, that means it isn't a link. If there isn't, that means it is still a potential link.






