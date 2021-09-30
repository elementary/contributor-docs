---
description: Tips for getting your pull requests reviewed
---

# Proposing Code Changes

## Write a Good Description

Your PR description should make it easy for a reviewer to know what they are reviewing before they see the code. To avoid wordy descriptions, use bulleted lists to describe changes. When appropriate, add a screenshot or a short video that makes your change more obvious. Good descriptions cut time on the time a reviewer needs to invest and makes your PR more attractive.

If it's not obvious, it can also be helpful to include instructions on how to test your PR, including any pre-requisites or dependencies.

## Review Your Own Branch

When you have your initial version for the proposed change working, look at your changes once again and ask yourself if anything could be improved before marking it "Ready for Review".

{% hint style="info" %}
If you need help or your branch isn't quite ready for review, you can open a Draft pull request and convert it to "Ready for Review" later
{% endhint %}

## Propose Minimum Viable Branches

The most helpful advice for getting your code reviewed and merged quickly is to keep your diff as small as possible. Small diffs are less intimidating for reviewers, easier to test, easier to read, and have a much smaller chance of regression.

{% hint style="info" %}
When proposing big changes, breaking up your work into several smaller pull requests is still considered best practice. Consider linking to an issue or discussion that explains the overarching goal.
{% endhint %}

## Program for The Present

Proposed changes should generally only implement things that are _actually_ needed right now, not just when you foresee that they _may_ be needed in the future. This is known [YAGNI](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)—You aren't gonna need it. Combined with continous refactoring, the YAGNI principle keeps the code base as simple as possible while helping us to avoid technical debt.

## Avoid Mixing Refactor and Functional Changes

It can be tempting to refactor code as you go, but this can make it harder for a reviewer to see what has been changed in your branch. If you need to refactor some code in order to make your change, consider submitting multiple PRs or separate refactoring commits from functional change commits and make it clear that you've done this in your pull request description. This extra step makes it much easier for another person to review your changes and minimizes the risk of regression.

{% hint style="info" %}
It's possible to clean up your Git history after the fact with [Interactive Rebasing](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History).
{% endhint %}

## Keep Function and Class Names Consistent

Naming is one of those things that feels trivial but really helps in a few years when it's all new eyes on some code. It can make it much easier to figure out what's happening if we use names that are self explanatory and not too generic, especially if the names feel similar to those used in platform libraries like GLib and GTK.

## Comment Non-Obvious Code

Code comments should be used any time it's not immediately clear _why_ something is being done. Comments shouldn't be used to describe obvious changes.

