# Lab Report 4
## Links to repositories
[Link to my repository](https://github.com/parth4apple/markdown-parse)

[Link to repository I reviewed](https://github.com/atruong39/markdown-parse)

## Snippet 1
What the test should produce: ``["`google.com", "google.com", "ucsd.edu"]``

Code in MarkdownParseTest.java for how I turned it into a test:
![code for snippet 1 testing](./labreport4assets/img1.png)

My implementation's error from junit:
![my error snippet 1](./labreport4assets/myerror1.png)

The implementation I reviewed's error from junit:
![their error snippet 1](./labreport4assets/theirerror1.png)



## Snippet 2
What the test should produce: `["a.com", "a.com(()), example.com"]`

Code in MarkdownParseTest.java for how I turned it into a test:
![code for snippet 2 testing](./labreport4assets/img2.png)

My implementation produces the expected output for snippet 2.

The implementation I reviewed's error from junit:
![their error snippet 2](./labreport4assets/theirerror2.png)

## Snippet 3
What the test should produce: `["https://ucsd-cse15l-w22.github.io/"]`

Code in MarkdownParseTest.java for how I turned it into a test:
![code for snippet 3 testing](./labreport4assets/img3.png)

My implementation's error from junit:
![my error snippet 3](./labreport4assets/myerror3.png)

The implementation I reviewed's error from junit:
![their error snippet 3](./labreport4assets/theirerror3.png)


## Analysis on fixing my implementation
### Snippet 1
With my implementation, it would be a minor change to account for backticks. I just need to create something that keeps track of the next backtick and if there is another one, to ignore the text between the two when looking for links. This can be done with a simple while loop similar to the one that checks for valid parenthesis. 

### Snippet 2
My implementation works for the snippet 2, and should work for other cases where there are nested parenthesis or nested brackets as well, since I have a valid parenthesis checker.

### Snippet 3
My implementation would only require a small change (<10 lines) in order for it to work with line breaks like the ones present in snippet 3. I would need to check that currentIndex is not out of bounds and if it is, to terminate the loop. Also, I would need to add a `\n` checker to make sure that links containing that character are not added to the list. This should only take a few if statements for both tasks.

