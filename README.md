# Git commit message

How to write a great Git commit message:

1. Begin the commit message with a short title that summarizes the change.

2. Start the title with an imperative present active verb: Add, Fix, Optimize, etc.

3. Format the title: start with a capital word, use up to 50 characters, and end without a period.

4. Optionally follow the title by a blank line, then a more thorough description. 


## Title examples

Title examples of good commit messages:

  * Add feature for foobar
  * Drop feature for foobar
  * Fix bug when foobar is missing
  * Bump version of foobar dependency
  * Make foobar integration script
  * Start foobar feature flag
  * Stop foobar feature flag
  * Refactor foobar for clarity
  * Reformat foobar to remove whitespace
  * Optimize foobar for speed and memory
  * Document foobar protocol


## Specifics

Capitalize the title.

* Right: Add feature
* Wrong: add feature

Do not end the title with a period:

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



## Imperatives

My team uses a title convention that helps us read fast, and helps us write tools to parse messages.

We agree on a short list of imperatives i.e. imperative mood, present tense, active voice, verbs:

* Add = Create a capability e.g. feature, test, dependency.
* Drop = Delete a capability e.g. feature, test, dependency.
* Fix = Fix an issue e.g. bug, typo, accident, misstatement.
* Bump = Increase the version of something e.g. a dependency.
* Make = Change the build process, or tools, or infrastructure.
* Start = Begin doing something; e.g. enable a toggle, feature flag, etc.
* Stop = End doing something; e.g. disable a toggle, feature flag, etc.
* Refactor = A change that MUST be just refactoring.
* Reformat = A change that MUST be just formatting, e.g. omit whitespace.
* Optimize = A change that MUST be just about performance, e.g. speed up code.
* Document = A change that MUST be only in the documentation, e.g. help files.


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
