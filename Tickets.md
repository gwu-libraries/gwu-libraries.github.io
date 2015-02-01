Tickets in Github
=================

We use Github tickets ("issues" in Github terminology) to define and track issues and potential issues at the repository level.

Tickets should generally be created:
- To note any defect observed in the application
- To suggest any feature or enhancement
- To define any feature or enhancement tasked for development
- To define non-coding tasks on which a milestone is dependent

Any code change pushed to a repository should be associated with a ticket, with only rare exceptions.

Any person in STG/LIT may create a ticket in an STG/LIT project repository.  Often our projects include partners outside STG/LIT, and those project team members may also create tickets in the appropriate repository.

Anatomy of a Ticket
-------------------

####Title:
- Ticket titles should be concise, clear, and as self-explanatory as possible.
- For suggested features or enhancements, consider beginning the title with the word "Consider".
- Titles may be updated/edited later as needed.

####Description:
- Descriptions should include #references to other tickets where appropriate.  This helps to navigate between cross-connected issues.  When mentioning other github users, use @mentions, as this will trigger Github to notify each user mentioned. (See [Github's guide to notifications, references, mentions, etc.](https://guides.github.com/features/issues/index.html#notifications).)
- Defects ("bugs") should include the following:
  - Steps to reproduce the defect, and any relevant context such as the environment/server where the defect was observed, the browser used
  - The result deemed defective
  - The expected result
  - When relevant, a screenshot
  - If possible, any potentially relevant areas of code identified

####Tags (Labels):
Tagging tickets is optional, but can be very useful.  These tags should be used when applicable:
- Bug (for defects)
- Enhancement
- Wontfix
- Proposed
- High Priority.  This tag can be useful for marking critical defects, and for highlighting "must do" enhancements for a milestone.

Multiple tags may certainly be applied to a ticket.

Ad-hoc tags may be created and used as appropriate per project.

A useful feature of Github is the ability to filter issues by label.

####Assignee:
- When creating a ticket, this may (and often should) be left empty
- The Assignee is generally assigned by the project manager, although it depends highly on the project.

####Milestone:
- The Milestone is generally assigned by the project manager.

Pull Requests Are Github Issues (Tickets) Too
---------------------------------------------

As far as Github is concerned, a Pull Request ("PR") is just another type of Issue.   We like the creator of a Pull Request to include:
- A reference back to the ticket, for easier navigation (e.g. "refs #123")
- Notes telling the tester how to test the PR

