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
Rules regarding`subject`:

* use imperative, present tense (eg: use "add" instead of "added" or "adds")
* don't use dot (`.`) at end
* don't capitalize first letter

---
# References
 
* [https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow
-1709](https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow
-1709)
* [https://365git.tumblr.com/post/3308646748/writing-git-commit-messages](https://365git.tumblr.com/post/3308646748/writing-git-commit-messages)
* [https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)