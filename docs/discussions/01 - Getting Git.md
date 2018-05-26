Before we begin, make sure you have Git installed on your computer. You can check it out through your command prompt or terminal.

```shell
$ git --version
```

It should display the Git version installed on your computer.

```shell
git version 2.14.1.windows.1
```
# Installation

For Mac OS X and Windows users, just download and run the following stand-alone installers:

* [Git for Mac installer](https://sourceforge.net/projects/git-osx-installer/files/)
* [Git for Windows installer](https://git-for-windows.github.io/)

For Linux users, if you are using Debian/ Ubuntu, install Git using `apt-get`:

```shell
$ sudo apt-get update
$ sudo apt-get install git
```

If you are using Fedora, install Git using dnf (or yum, on older versions of Fedora):

```shell
$ sudo dnf install git
```
or
```shell
$ sudo yum install git
```

# Git config

Once you've verified that the installation has been successful by typing `git --version`, configure your global Git username and email:

```shell
$ git config --global user.name "Your Name"
$ git config --global user.email "yourname@email.com"
```

# Didn't quite Git it?

Feel free to ask and participate in our [Gitter chat room](https://gitter.im/WWCodeManila/Git)!

# References

* https://www.atlassian.com/git/tutorials/install-git
