## Collaborating with teams

* Code review
* Project management
* Documentation

* Adding and removing collaborators on GitHub

## Branching

Nearly every VCS has some form of branching support. Branching means you diverge from the main line of development and continue to do work without messing with that main line. In many VCS tools, this is a somewhat expensive process, often requiring you to create a new copy of your source code directory, which can take a long time for large projects.

Some people refer to Git’s branching model as its *killer feature*, and it certainly sets Git apart in the VCS community. Why is it so special? The way Git branches is incredibly lightweight, making branching operations nearly instantaneous, and switching back and forth between branches generally just as fast. Unlike many other VCSs, Git encourages workflows that branch and merge often, even multiple times in a day. Understanding and mastering this feature gives you a powerful and unique tool and can entirely change the way that you develop.

1. Open your console and navigate to the location of your forked `git-party`.

```shell
$ cd <path-to-directory>
```

2. Check the branches available on your local copy.

```shell
$ git branch
```

Right now, you only have the `master` branch.

3. Check the all of the branches available on both your local and remote repositories.

```shell
$ git branch --all
```

You should be able to see something like this:

```shell
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/christine
  remotes/origin/issa
  remotes/origin/alysson
```

This indicates that you have 4 branches: `master`, `christine`, `issa` and `alysson`, on your remote named `origin`.

3. Create your own local branch and push it to your remote repository.

```shell
$ git checkout -b <your-name> master
$ git push origin <your-name>
```

This switches you to a new branch called `<your-name>` on your local copy which contains what's exactly in `master`. You can verify it by using `git branch` again.

To switch back and forth between local branches, use `git checkout <branch-name>`.

To checkout a remote branch, fetch it first using `git fetch <branch-name>` before checking it out using `git checkout <branch-name>`.

4. Pull the changes from `alysson`.

```shell
$ git pull origin alysson
```

Pulling basically *gets* and integrates the changes made on a remote branch to the local branch that you have checked out.

Pulling changes before editing and/or committing helps in avoiding conflicts, especially when people are working on the same parts of a single file.

5. Open `20180526.md` under the `today-i-learned` folder. Add what you learned about Git today or what you liked the most about our Git party. Sign it off with your name and GitHub account!

```shell
* "A git pull a day keeps the conflicts away." - [Alysson Alvaran](https://github.com/alyssonalvaran)
```

6. Add and commit it to your local repository.

```shell
$ git add "today-i-learned/20180526.md"
$ git commit -m "Add what I learned today"
```

7. Checkout the `master` branch and merge your changes from your `<your-name>` branch.

```shell
$ git checkout master
$ git merge <your-name>
```

Unlike pulling, merging gets the changes from the local branch that you've specified. This is helpful when you're working on a different branches locally.

8. Now that you've merged the changes to your `master` branch, try deleting `<your-name>` locally.

```shell
$ git branch -d <your-name>
```

Since you've pushed `<your-name>` to your remote repo earlier, if you try to get the list of all available branches via `git branches --all`, you'll see that `<your-name>` still exists remotely.

9. Delete your branch remotely as well.

```shell
$ git push origin --delete <your-name>
```

10. Finally, create a pull request in the orginal `git-party` repository!

# Congratulations!

You can now collaborate with your friends on GitHub!

Do you have an awesome project in mind? Share it with us and who knows, people might just get interested in collaborating with you and contributing to your project!

# Didn't quite Git it?

Feel free to ask and participate in our [Gitter chat room](https://gitter.im/WWCodeManila/Git)!

# References

* https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell
* http://dont-be-afraid-to-commit.readthedocs.io/en/latest/git/commandlinegit.html
* https://www.atlassian.com/git/tutorials/using-branches/git-merge