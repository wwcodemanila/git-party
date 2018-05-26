# What is a repository?

A **Git repository** or *repo* is a virtual storage of your project. It allows you to save versions of your code, which you can access when needed. 

# Creating a repository

1. Log in to your [GitHub](https://github.com) account.

2. Click the **+** button on the upper right corner of the page and select `New repository`.

3. Name your repository `my-first-repo` and check `Initialize this repository with a README`.

4. Click `Create repository`.

<img src="https://github.com/alyssonalvaran/git-party/blob/master/docs/assets/repo-create.png" alt="repo-create" style="height: 200px"/>

*Mabuhay*! You now have a new repository named `my-first-repo` with a `README` markdown file.

<img src="../assets/repo-new.png" alt="repo-new" style="height: 200px"/>

# Cloning a repository

Now that you have a remote repository on GitHub, it's time to get a local copy on your computer.

**Cloning** is the most common way for users to obtain a local copy of a remote repository with existing files.

*If you're working with an empty repository, you need to initialize it using `git init` to get a local copy. For more information, you can check out this [interactive tutorial](https://try.github.io) by Code School and GitHub.*

1. Go to the repo that you created on GitHub and click on the green `Clone or download` button.

<img src="../assets/repo-clone.png" alt="repo-clone" style="height: 100px;"/>

2. Copy the HTTPS link by clicking the copy button or selecting the link and pressing `CTRL + C`.

3. Open your console and go to the path where you want to place the local copy of your repository.

```shell
$ cd <path-to-directory>
```

*Bonus*: If you're using bash, type `pwd` to get the present working directory. If you're using cmd, type `cd` instead.

4. Clone the repository using `git clone`.

```shell
$ git clone <repository-https-link>
```

Ta-da! You can now check the directory where you placed your local copy. You should see a folder with named `my-first-repo` with the `README` file inside.

# Editing files

Before you start editing, make sure you're familiar with the following terms:
- [x] text editor
- [x] markdown
- [x] README


## Text editors

A **text editor** is any word processing program that you can use to type and edit text.

Commonly used text editors:
* [Notepad++](https://notepad-plus-plus.org/)
* [Sublime Text](https://www.sublimetext.com/)
* [Atom](https://atom.io/)
* [Visual Studio Code](https://code.visualstudio.com/)

## Markdown

**Markdown** is a way to style text on the web. You control the display of the document; formatting words as bold or italic, adding images, and creating lists. Mostly, markdown is just regular text with a few non-alphabetic characters thrown in, like # or *.

This file is also created using markdown, thus the `.md` file extension!

## README

You can add a README file to your repository to tell other people why your project is useful, what they can do with your project, and how they can use it.

A README file, along with a [repository license](https://help.github.com/articles/licensing-a-repository), [contribution guidelines](https://help.github.com/articles/setting-guidelines-for-repository-contributors), and a [code of conduct](https://help.github.com/articles/adding-a-code-of-conduct-to-your-project), helps you communicate expectations for and manage contributions to your project.

A README is often the first item a visitor will see when visiting your repository. README files typically include information on:

* What the project does
* Why the project is useful
* How users can get started with the project
* Where users can get help with your project
* Who maintains and contributes to the project

If you put your README file in your repository's root, `docs`, or hidden `.github` directory, GitHub will recognize and automatically surface your README to repository visitors.

Here's an example of a good [README template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2).

## Activity!

1. Open the `README` file inside `my-first-repo` using your favorite text editor, preferably one that allows markdown preview.

2. Add the following text below "`# my-first-repo`":

```shell
This is a sample repository.

# Authors

* [Alysson Alvaran](https://github.com/alyssonalvaran)
```

Note: `#` translates to the HTML `<h1>` tag, `##` translates to `<h2>`, and so on. `*` translates to a bullet and `[text](link)` allows you to insert a hyperlink to a text.

If you don't have a markdown preview feature on your text editor, you can paste your codes [here](http://markdownlivepreview.com/) to see what it looks like.

# Pushing changes

Now that you're done editing, our final step is to *push* to changes back to the remote repository.

**Pushing** uploads your local *commits* to your remote repository.

1. Open your console and check the unstages changes that you made.

```shell
$ git status
```

2. Add the file to be committed using `git add <filename>`.

```shell
$ git add README.md
```

You may also use `git add --all` to add all of the unstaged and untracked files if you're working on multiple files at a time.

3. Commit the staged changes to your local repository using `git commit -m <commit-message>`.

```shell
$ git commit -m "Initial commit"
```

*Bonus*: You can use `git log` to display the list of commits that you've made so far.

4. Finally, push your commit to the remote repository using `git push <remote> <branch>`.

```shell
git push origin master
```

`origin` is the default remote created by GitHub that corresponds to the URL of your repository while `master` is the default branch. You'll learn more about these in the next lessons.

# Congratulations!

You've successfully created and pushed your changes to your first repository!

# Didn't quite Git it?

Feel free to ask and participate in our [Gitter chat room](https://gitter.im/WWCodeManila/Git)!

# References

* https://www.atlassian.com/git/tutorials/setting-up-a-repository
* https://try.github.io
* https://guides.github.com/features/mastering-markdown/
* https://techterms.com/definition/texteditor
* https://help.github.com/articles/about-readmes/