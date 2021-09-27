---
description: Guidelines to make code reviews fruitful for developers and reviewers alike
---

# Reviewing Code

Code reviews play a crucial role in the development process. Having other people verify your code not only improves overall code quality, it serves an even bigger purpose: providing an opportunity to learn from each other. This guide aims to lower the barrier to reviewing code by providing a common ground of best practices and philosophies which have proved to be useful over the years.

{% hint style="info" %}
The roles of developer and reviewer are not mutually exclusive—you can be both. And we highly encourage you to perform both roles, because this leads to more diverse reviews which help us to improve the overall user experience of elementary OS.
{% endhint %}

### A Partial Review Is Better Than None

You don't need to fully understand the codebase to test its functionality. Often the feedback provided by a partial review helps to keep the momentum and multiple partial reviews eventually lead to a full review.

### It's Okay to Ask Questions

If there's code you don't understand, ask about what it does. The chances are good it either needs a comment, could be refactored, or you get to learn something new!

### Watch for Potential Points of Failure

Because of Murphy's law \("Anything that can go wrong will go wrong"\) we want to make extra sure to keep an eye on potential pitfalls during code review. This is especially true for code that is responsible for carrying out a user's intent. Code which fails to execute a user initiated action _and_ is unable to inform the user about the error leads to a bad experience.

### Recognize The Good Things

If you come across something you like about a proposed change, don't hesitate to let the developer know. Its just more fun to work with people who recognize the effort made.

