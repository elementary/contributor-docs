---
description: >-
  elementary uses GitHub to track issue reports and feature requests publicly.
  You can send feedback to the team to inform us of a problem you encountered or
  an improvement that you would like to see.
---

# Reporting Issues

## Using The Feedback App

To get started with issue reporting, open "System Settings" and navigate to the "System" page. Select "Send Feedback", which will open the Feedback app. From here, choose a category that best describes the general area of the issue, and then choose a specific project to open a new issue against. This will open your web browser to the relevent GitHub page where you can view and create new issue reports.

{% hint style="info" %}
If you can't find a specific project or aren't sure which project to file against, that's okay! Do your best and if the issue report needs to be migrated to a different project, a bug manager will take care of it for you.
{% endhint %}

You can also see a list of all elementary Github projects on [this page](https://github.com/elementary) and search for projects here. When you've found the project you'd like to open a new report against, open it and then select the "Issues" tab.

## Creating a New Issue Report

When filing a new report, it's a good idea to search the issue list to make sure your report hasn't been filed already. If your report has already been filed by someone else, you should add the 👍️ reaction to the report to indicate that you are also affected. 

{% hint style="warning" %}
Only comment on an existing issue report if you can provide additional useful information that may help track down the source of the issue. Do not comment things like "I have this problem too" or "This is a really important issue"
{% endhint %}

If your report has not already been filed, select the green "New Issue" button at the top right corner of the "Issues" page. Keep in mind the following information while filing your report:

### Be Specific In The Summary

This will be the title of the issue on the issues page. It's important to be specific because it makes it much easier for a developer or bug manager to search the issue list and helps avoid duplicate reports.

❌️  _"Performance is bad"_

This summary is too vague and could possibly describe a number of different issues.

✅️  _"UI is unresponsive while importing"_

This summary describes the specific case where we're experiencing a performance issue and what that issue is in a concise way.

Your issue summary should also not include things in brackets like "\[bug\]" or "\[feature request\]". elementary uses labels to categorize issue reports.

### Describe The Problem Objectively

The most important thing for an issue report is making sure that a developer will be able to understand and reproduce the issue that you're facing. Describe what happened and contrast it with what you expected to happen instead. If necessary, include exact numbered steps to reproduce the issue.

❌️  _"Queuing is unintitive. I don't like the way it works"_  

This description leaves too much room for interpretation and doesn't specifically describe a problem that can be resolved.

✅️  _"When I add items to the queue, they appear at the top. I expected them to appear at the bottom instead"_ 

This describes a problem in a way that is actionable and objective and explains how to reproduce the issue.

### Be Prepared To Provide More Information

Include relevant information like your OS version or any modifications you've made to the system \(like changing your window manager or kernel\). If you're reporting a crash, make sure to [include a backtrace.](inspecting-crashes.md)

If your report does not contain enough information for a developer to reproduce the issue, it may be labeled as "Incomplete".  If it is, a developer will make a comment requesting additional specific information. If you do not provide that information, your report will eventually be closed since it is unable to be acted upon as filed.

### You Can Get a Bit of Help

If you're not sure about anything above, you are always welcome to chat with community members and developers in the [Community Slack](https://community-slack.elementary.io/). We might be able to help you track down the project where you should report an issue, or perhaps even aid you with any English language issue you might come across. Most developers want to help you make good bug reports.

## Creating a New Feature Request

elementary uses GitHub Issues both for reporting problems and for tracking feature requests. In addition to what's been mentioned above, keep in mind the following tips when creating new feature requests:

### Describe The Problem

It's often tempting when creating a feature request to only describe the proposed solution, but don't forget to fully describe the problem that your proposal is meant to solve. Describing the problem is an essential step to ensure that a proposed design meets its goals.

{% hint style="info" %}
If you're having trouble describing the problem in a concise way or it involves a larger design change rather than a single new feature, consider [starting a discussion](../starting-discussions.md) instead
{% endhint %}

### Include Mockups or Prior Art

If you can, include a mockup or a sketch of what your proposed new feature would look like. Or, if there's another project that implements this feature, include screenshots or links to that project.

### Consider Alternatives

If there could be alternative solutions to your intial problem, describe them and their merits. A developer may decide that a certain specific feature request is out of scope for a project or conflicts with its other design goals, but if you include alternative solutions one of those may work better and be accepted as a solution.

