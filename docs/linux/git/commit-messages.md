# Git Commit Messages
## Naming Convention
### Intro
Motivation of this page is to curate all information at one place and to make more people aware about standards followed by industry.
### Convention
A typical git commit message will look like

```shell
<type>(<scope>): <subject>
```
#### type
`type` must be one of the following mentioned below!

* `build`: Build related changes (eg: npm related/ adding external dependencies)
* `chore`: A code change that external user won't see (eg: change to . 
  gitignore file or .prettierrc file)
* `feat`: A new feature
* `fix`: A bug fix
* `docs`: Documentation related changes
* `refactor`: A code that neither fix bug nor adds a feature. (eg: You can 
  use this when there is semantic changes like renaming a variable/ function name)
* `perf`: A code that improves performance
* `style`: A code that is related to styling
* `test`: Adding new test or making changes to existing test

#### scope
Example `<scope>` values:

* `init`
* `runner`
* `watcher`
* `config`
* `web-server`
* `proxy`
* ... etc.

The <scope> can be empty (e.g. if the change is a global or difficult to assign to a single component), in which case the parentheses are omitted. In smaller projects such as Karma plugins, the <scope> is empty.

#### subject

The first line cannot be longer than 70 characters, the second line is always blank and other lines should be wrapped at 80 characters. The type and scope should always be lowercase as shown below.

Rules regarding`subject`:

* use imperative, present tense (eg: use "add" instead of "added" or "adds")
* don't use dot (`.`) at end
* don't capitalize first letter

#### message footer
###### Referencing issues
Closed issues should be listed on a separate line in the footer prefixed with "Closes" keyword like this:
```shell
Closes #234
```
or in the case of multiple issues:
```shell
Closes #123, #245, #992
```
###### Breaking changes
All breaking changes have to be mentioned in footer with the description of 
the change, justification and migration notes.

```shell
BREAKING CHANGE:

`port-runner` command line option has changed to `runner-port`, so that it is
consistent with the configuration file syntax.

To migrate your project, change all the commands, where you use `--port-runner`
to `--runner-port`.
```

### Examples

```shell
fix(middleware): ensure Range headers adhere more closely to RFC 2616

Add one new dependency, use `range-parser` (Express dependency) to compute
range. It is more well-tested in the wild.

Fixes #2310
```

---
# References
 
* [https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow
-1709](https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow
-1709)
* [https://365git.tumblr.com/post/3308646748/writing-git-commit-messages](https://365git.tumblr.com/post/3308646748/writing-git-commit-messages)
* [https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)