# Git Commit Messages
## Naming Convention

Motivation of this page is to curate all information at one place and to make more people aware about standards followed by industry.

A typical git commit message will look like

```shell
<type>(<scope>): <subject>
```
"type" must be one of the following mentioned below!

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

---
Sources
 
* <sub>[https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow
-1709](https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow
-1709)</sub>