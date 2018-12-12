# Atlassian Jira "smart commits"

https://confluence.atlassian.com/fisheye/using-smart-commits-298976812.html

The general idea of Atlassian Jira "smart commits" is to put Jira-related meta-data into the git commit message.

Syntax:

    <ISSUE_KEY> #<COMMAND_1> <optional COMMAND_1_ARGUMENTS> #<COMMAND_2> <optional COMMAND_2_ARGUMENTS> ... #<COMMAND_n> <optional COMMAND_n_ARGUMENTS>

Example:

    JRA-999 #time 1w 2d 4h 30m #comment Task completed ahead of schedule #resolve

Our opinion is that Jira "smart commits" are not smart, and should never go in the summary line, because the purpose of the git summary line is for a subject akin to an email. The git documentation is clear on this, Linus is clear on this, and most importantly the reasoning is sound. The goal of the git summary line is to summarize, for fast easy readability.

Our opinion is that time tracking information belongs in your product management tool (e.g. Jira) rather than in git commit messages, because the time tracking information is irrevelant to the code.

If your team chooses to use the Jira syntax, then we suggest you put the syntax into the git commit message body.

Example:

    Add feature foo

    JRA-999 #time 1w 2d 4h 30m #comment Task completed ahead of schedule #resolve

If your team really wants to link the git commit message to the product management tool, then consider using the best way that we've found to accomplish this, which is to simply add the link at the start of the body.

Example:

    Add feature foo

    https://my.atlassian.net/browse/JRA-999

    JRA-999 #time 1w 2d 4h 30m #comment Task completed ahead of schedule #resolve
    
You can create a [git commit template](https://github.com/joelparkerhenderson/git_commit_template) to make it fast to add Atlassian Jira "smart commits" as you like.
