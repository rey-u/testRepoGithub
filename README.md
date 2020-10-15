# testRepoGithub

## HINAKO

## getting started
| Command                                  | Action 
| :--                                      | :--
|`git` config --global user.name *name*    |set user name
|`git` config --global user.email *email*  |set user email
|`git` init                                |initialize a git directory
|`git` remote add origin *URL*             |create a new remote called origin


## informational
| Command                       | Action
| :--                           | :--
|`git` --version                |display git version
|`git` config --global --list   |list config settings
|`git` remote - v               |display remote URL 
|`git` branch -a                |list branches
|`git` status                   |display changes and staging
|`git` log                      |view commit history and hashes


## common tasks
### navigating
| Command                       | Action
| :--                           | :-- 
|`git` branch *name*            |create branch with *name*
|`git` branch -d *name*         |delete branch *name*
|`git` checkout *name*          |perform changes in *name*
|`git` checkout -b *name*       |create and checkout a new branch
|`git` checkout master          |
|`git` reset HEAD^1             |move HEAD back 1 commit (note you can't push from this: see `revert`)
|`git` revert *hash*            |undoes changes made since *hash* and _then_ commits (to allow for push)
|`git` pull origin master       |
|`git` merge *name*             |merge current (checked out) branch with *name*
|`git` diff                     |see the line by line differences between local and repo


### staging committing and pushing
| Command                           | Action
| :--                               | :-- 
|`git` add -A                       |add all modified files to staging
|`git` tag *name*                   |label (tag) the current commit as *tag*
|`git` commit -m "*message*"        |commits the files in staging
|`git` commit --amend               |modify the previous commit with the files in staging
|`git` push origin --delete *name*  |push to origin and delete branch *name*
|`git` push origin master           |push to origin the branch *master*
|`git` push -u origin *name*        |push to origin the branch *name* and set origin as upstream
|`git` push --set-upstream origin master  |see above


![Dancing Pikachu](https://media.tenor.com/images/61963600f685f92d0d7efb4eb4ea72c5/tenor.gif "Dancin' 'chu)

## typical workflow
| Task                                 | Command
| :--                                  | :-- 
|create new branch to make edits       |`git` checkout -b *new-branch*
|add edits to staging and commit       |`git` add .
|                                      |`git` commit -m "*commit message*"
|move to master and update             |`git` checkout master
|                                      |`git` pull
|merge branch with updated master      |`git` merge *branch-name*
|delete working branch                 |`git` branch -d *branch-name*
|push updated master to remote repo    |`git` push origin master

## Update a forked repo on GitHub
As your fork only exists on GitHub, and GitHub does not have tools for doing merges through the web interface, you must do the upstream merge locally and then push the changes back to your fork.

1. `git` remote add upstream *URL*
1. `git` fetch upstream
1. `git` checkout master 
1. `git` rebase upstream/master
1. `git` push -f origin master

### Jim Parker's recipe

```bash
git checkout master
git fetch upstream
git reset --hard upstream/master
git push origin master --force
```

Creates new branches for tasks.
Push branches to remote fork (avoid merging master).


## What is a commit?
   commit  
   (n) A single point in the Git history; the entire history of a project is represented as a set of interrelated commits. The word "commit" is often used by Git in the same places other revision control systems use the words "revision" or "version". Also used as a short hand for commit object.  
   (v) Storing a new snapshot of the project’s state in the Git history by creating a new commit representing the current state of the index and advancing HEAD to point at the new commit.  
Source: [gitglossary][1]

[1]: https://git-scm.com/docs/gitglossary


![git commands conceptualization](git-commands.png)


`git pull` ~= `git fetch` + `git merge FETCH_HEAD`  
`git pull` merges into the _current_ branch  
`git push` does not automatically merge

[Click here](#HINAKO) to go to the **Hinako** header