# Proposing Design Changes

elementary has always been known for its strong focus on great design, but if you’re an up and coming designer you might not know how to get developers to pay attention to you. This reference guide is about how to effectively propose a design change in a way that makes it more likely for your design to become implemented.

### Don't Make Demands <a id="dont-make-demands"></a>

Let’s say you spent the last few hours re-designing the Search Engine Manager dialog in Midori and you want to bring this work to the attention of Midori’s developers. You could file a bug report something like “Search engine popup sucks” and paste your mockup and be done. But that approach isn’t going to win you any friends and your report will probably be marked “opinion” or “invalid”. Instead, we should consider the amount of work it will take to implement the new design and try to present it in a way that gets developers excited about the overall vision without demanding 1,000 lines of code in one shot.

### Open a GitHub Issue <a id="open-github-issue"></a>

If you have an idea for a new design that you think would improve a project, file an issue on the respective GitHub repository with your proposal. This will get a response from a team member and will start the design process. Name your issue something explicit and try to avoid titles that marginalize developer’s existing work. Something like “search engine manager redesign” works just fine. In this issue we want to describe our motivations for the redesign. What are the problems with the current design and what does our new design aim to solve? Common reasons for a redesign can include minimizing window chrome, taking advantage of new toolkit elements, making the UI more consistent with other apps, etc. This is also a good place to link to or attach that mockup we were talking about earlier. If your design is really involved, you can even link to an external specification—Google Docs work great for getting feedback, or you can use the GitHub Wiki for the repository—where you have a chance to really get into the nitty gritty of your idea. If you make a good case for your proposal, the team will tag your issue with `Needs Design` and `Confirmed` labels, plus possibly assign the UX team for a review.

Keep in mind many aspects of a design in elementary OS have had years of thought and iteration behind them, so contributors may be hesitant to sweeping redesigns. Small, more iterative improvements are often much easier to come to a conclusion on and implement if approved.

{% hint style="info" %}
Need help opening an issue? Take a look at [Reporting Issues](reporting-issues.md)
{% endhint %}

### Create Concise Work Items <a id="create-concise-work-items"></a>

Now that you’ve laid out the motivations for your design and explained the overall vision, you should break it up into small, actionable work items \(these can be included as subtasks on your issue or as separate issues\). To continue our example, I would have issues like “Change Search Engine Manager Dialog to Popover”, “Re-order Search Engines with Drag and Drop”, “Open Search Engine Manager by clicking Search icon in URL Bar”, “Show edit and remove buttons next to engine in Search Engine Manager”, etc. Each issue should describe just one small change. We do this for several reasons:

* It allows developers to deny one request without denying all of them. Face it: your design isn’t perfect and it’s very possible that a developer isn’t going to like part of it. By breaking up your design into little pieces, it allows a developer to incorporate the changes they like and ignore the ones they don’t.
* It makes your design less intimidating. A big redesign means lots of lines of code. If your changes look like too much of a hassle, you’re going to have a hard time getting a developer to work on them. But if you present small changes that can be incorporated a bit at a time, there’s a bigger chance that your whole design will eventually be implemented.
* It allows developers to track their progress. Once again, big designs take time to implement. Even if a developer wants to implement the whole thing right away, they might not be able to. Giving them a way to “check off” pieces as they go makes it more likely that a part of your design won’t be forgotten about when it’s translated into code.

### File Compelling Reports <a id="file-compelling-reports"></a>

Don’t forget to make your reports compelling. It’s up to you to sell the merits of each change. Cite the HIG, prior-art, user complaints, articles by other designers, and present your changes in a logical, non-opinionated, and concise manner. It also doesn’t hurt to speak in developer terms. Brush up on the names of widgets in Gtk and Granite, get familiar with available libraries like Zeitgeist and Unity, and don’t forget about system components like PulseAudio or Contractor.

### Be Prepared to Iterate <a id="be-prepared-to-iterate"></a>

Don’t be upset if a developer plainly states that they don’t want to implement your idea. Remember that they have plans too. You might have to go back to the drawing board a bit. Listen to their feedback. Your design might be a little over-engineered, it might conflict with other designs being worked on, or maybe it’s just in conflict with the goals and scope of the app. Remember that you’re in the position of requesting someone to devote their time to something. You’re asking for a favor. Don’t be afraid to argue a position within polite reason, but remember to stay humble.

### Tracking Proposals <a id="tracking-proposals"></a>

Lets say you've convinced the developers of the merits of your new design, how do you keep track of the progress? GitHub has a projects feature for tracking issues and their progress as apart of larger initiaves. Projects are managed on a per-repository basis at each individual GitHub repository \(check out the projects board for this website [here](https://github.com/elementary/website/projects)\) and by the elementary organization \(check out elementary's projects [here](https://github.com/orgs/elementary/projects)\) to track initiaves across projects. Projects are maintained by the owner of the GitHub repo or by elementary and link back to the issues you've created.

