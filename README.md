# Git commit message

To write a great git commit message, take a look at these guidelines and suggestions.


## Top priorities

For the best git commit messages:

  * Read these guidelines and suggestions, then discuss them with your teammates.

  * Emphasize clear communication, because commit messages help you and your teammates.
  
  * Use a git commit template such as our file [git_commit_template.txt](doc/git_commit_template.txt)


## Begin with a short summary

For the short summary line a.k.a. message subject:

  * Start with an imperative present active verb: Add, Drop, Fix, Refactor, Optimize, etc.

  * Use up to 50 characters; this is the git official preference.
  
  * Finish without a sentence-ending period.


## Continue with a longer description

For the longer description lines a.k.a. message body:

 * If you want to write more, then add a blank line after the title, and write as much as you want.
  
 * Use up to 72 characters per line for typical text for word wrap.

 * Use as many characters as needed for atypical text, such as URLs, terminal output, formatted messages, etc.

 * Include any kind of notes, links, examples, etc. as you want.
  

## Title examples

Title examples of good commit messages:

  * Add feature for foo
  * Drop feature for foo
  * Fix foo when bar is missing
  * Start flag for foo
  * Stop flag for foo
  * Refactor foo for clarity
  * Optimize foo for speed and memory


## Keywords

We recommend these keywords because they use imperative mood, present tense, active voice, and are verbs:

* Add = Create a capability e.g. feature, test, dependency.
* Drop = Delete a capability e.g. feature, test, dependency.
* Fix = Fix an issue e.g. bug, typo, accident, misstatement.
* Bump = Increase the version of something e.g. a dependency.
* Make = Change the build process, or tools, or infrastructure.
* Start = Begin doing something; e.g. enable a toggle, feature flag, etc.
* Stop = End doing something; e.g. disable a toggle, feature flag, etc.
* Refactor = A change that MUST be just refactoring.
* Reformat = A change that MUST be just formatting, e.g. omit whitespace.
* Rephrase = A change that MUST be just textual, e.g. edit a comment, doc, etc.
* Optimize = A change that MUST be just about performance, e.g. speed up code.
* Document = A change that MUST be only in the documentation, e.g. help files.


## Semantic versioning

We use semantic versioning for many of our projects:

* Add = Increment SemVer MINOR version.
* Drop = Increment SemVer MAJOR version.
* Fix, Refactor, Reformat, Rephrase, Optimize, etc. = Increment SemVer PATCH version.


## Specifics

Capitalize the title.

* Right: Add feature
* Wrong: add feature

Do not end the title with a period.

* Right: Add feature
* Wrong: Add feature.

Use imperative mood: present tense, active voice, and lead verb.

* Right: Add feature
* Wrong: Adds feature (this is indicative mood, not imperative mood)
* Wrong: Added feature (this is past tense, not present tense)
* Wrong: Adding feature (this lead is a gerund, not a verb)
* Wrong: Feature added (this is passive voice, not active voice)

Keep the title within 50 characters.

  * This is the git documentation convention.

Use a blank line after the title.

  * This is the same convention as writing an email message.

Wrap the body at 72 characters.

  * This is the same convention as writing an email message.

For more about these see [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)


## Reasoning

We primarily care that our team communicates effectively with our shared understanding. 

We secondarily like these verbs above because they're easy to read, easy to type, and clear in many cultures.

If you and your team prefer other words, that's fine too; use what works for you.


## Reject these formats

We reject some kinds of git commit message formats:

* [bug] ...
* (release) ...
* #12345 ...
* jira:// ...
* docs: ...

We reject the commit style of projets such as Angular, Commitizen defaults, etc.

  * Because these use a leading tag that is sometimes a word, sometimes an abbreviation, sometimes a plural noun, etc. 

  * Examples are using "feat" for feature, "docs" for document, "perf" for performance improvement, etc.

  * Instead we use "Add" for adding a feature, "Document" for documenting help, "Optimize" for performance improvement, etc. 

  * Active verbs are easier to skim, and easier to use for people from other cultures who may be less-comfortable using English.

We reject using an id number or URL in the title.

  * We use fully-qualified URLs in the commit message body.

  * This is because many of our projects use multiple tracking systems, and multiple ways of launching a URL. 

  * We want URL tracking to be easy to use by a wide range of systems, scripts, and teams.


## Optional: use contact email addresses

We sometimes have more than one person working on a commit. For example, we do do pair programming.

To keep track of this, we write a git commit message body that lists each person. We use the person's name and the email address. We use one person per line because this is easy to parse.

To make this easy in practice, we use a git template that helps fill in this info.

Example syntax for readability and compatibility:

    By: Alice Adams (alice@eaxmple.com)
    By: Bob Brown (bob@example.com)
    By: Carol Curtis (carol@example.com)

Example syntax for specific to GitHub automatic detection:

    Co-authored-by: Alice Adams <alice@eaxmple.com>
    Co-authored-by: Bob Brown <bob@example.com>
    Co-authored-by: Carol Curtis <carol@example.com>

Note: we have an open request for the GitHub team to do automatic detection of both syntaxes above.


## Optional: use task tracking links

We sometimes connect a git commit to a task tracking system or web page that explains more. For example, we use GitHub, Trello, Jira, and many other bug tracking systems and project management software systems.

To keep track of these, we use a git commit message body that lists each URL, one per line because this is easy to parse.

Example:

    Add feature foo

    See: https://github.com/user/repo/issues/789
    See: https://jira.com/tasks/123
    See: https://wikipedia.com/quicksort

If we want to provide link names, then we use Markdown links, such as:

    See: [Request for help with sign in](https://github.com/user/repo/issues/789)
    See: [Add feature foo](https://jira.com/tasks/123)
    See: [Wikipedia Quicksort](https://wikipedia/quicksort)

To make this easy in practice, we use a git template that helps fill in this info.


## Optional: use keywords, importance, references, etc.

We like to use commit message keywords to help us skim, search, and prioritize.

To keep track of these, we write a git commit message body that uses email header conventions.

Example:

    Fix foo

    Keywords: security, encryption, authentication
    Importance: high
    References: ...
    Supersedes: ...
    Obsoletes: ...
    See-Also: ...

We use some of these to help our teams focus on the most important work.

  * When a commit message says "Importance: high" then it gets priority for code review and also for testing on the continuous integration server.

  * When a commit message says "Supersedes", "References", "Obsoletes", then we can easily look up the earlier commits or URLs.


## Related links

* [5 Useful Tips For A Better Commit Message by Caleb Thompson at Thoughtbot](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)

* [A Note About Git Commit Messages by tpope at tbaggery](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)

* [How to Write a Git Commit Message by Chris Beams](https://chris.beams.io/posts/git-commit/)

* [Writing good commit messages by the Erlang OTP team](https://github.com/erlang/otp/wiki/writing-good-commit-messages)

* [On commit messages by Who-T](http://who-t.blogspot.com/2009/12/on-commit-messages.html)