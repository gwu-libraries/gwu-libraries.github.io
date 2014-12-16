Development task workflow
=====================

(for features, defects, etc. performed by the development team.)

In general, we follow the [Github Flow](http://scottchacon.com/2011/08/31/github-flow.html).  The following provides some additional clarifications on our flavor of the workflow:

1.  For each development task, a team member creates a [tickets](Tickets.md).  The ticket is assigned to a developer and optionally to a milestone.
2.  For each ticket, the developer creates a feature branch.  The feature branch should be named `t<ticket #>-<short description with words - separated>`, e.g., `t286-export-stream`.  For example, to create and checkout a feature branch:

        git checkout master
        git checkout -b t286-export-stream

    > Note:  In general, 1 development task = 1 ticket = 1 feature branch.  However, where appropriate, variations are acceptable.  In particular, a development task may be broken up into multiple tickets or multiple related tickets may be included in a single feature branch.

3.  Developer does work and commits to feature branch.  The developer is welcome to commit as often as necessary for development purposes.  A commit to a feature branch may result in the code being "broken".  Each commit must be accompanied by a descriptive message.

    Periodically, the developer should get the latest commits from master using rebase:
    
        git checkout mybranch
        git rebase master
        
4.  When completed with the task or wanting to collaborate with other team members, the developer pushes the branch to origin.

        git push -u origin mybranch
        
    **Caution:** If other developers are working on your branch and you rebase, you can really mess things up.  Once a feature branch has been pushed to origin, only rebase if no one else is working on it or are completed working on it.

5.  When completed with the task and ready for code review, the developer cleans up the commit history using interactive rebase and issues a pull request.

    The goal of the interactive rebase is to provide a clean history for other developers and to make sure that each commit to the master branch is stable.  The combined commit message should start with the by referencing the tickets (e.g, `fixes #75, #78`) and describe the entire code change.  While generally the commits should be squashed to one commit, depending on the code change, they may be squashed to multiple commits.  For more information on rebase, see [Using Git rebase](https://help.github.com/articles/using-git-rebase/).
    
    To create a pull request, in Github go to the branch and click the pull request button.  Note that the pull request creates a ticket.  The pull request ticket should be assigned to the tester.  A reference to the original ticket should be placed in the pull request ticket and a reference to the pull request ticket should be placed in the original ticket.  
    
6.  The tester reviews and test the code.  All comments should be placed in the pull request ticket.  For commenting on a pull request see [Commenting on the diff of a pull request](https://help.github.com/articles/commenting-on-the-diff-of-a-pull-request/).

    For minor fixes only, a tester a code reviewer may make, commit, and push changes to the pull request branch.
    
7.  Developer addresses issues, commits, rebases, and pushes changes.

    >These last two steps are repeated until all issues are addressed either by fixing or by documenting in additional tickets for later work.

8.  Tester accepts the pull request (from git command line or by pressing the merge pull request button).
9.  Team members with local copies of the feature branch delete them.