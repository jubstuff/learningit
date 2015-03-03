# Setting up your repository

```
git config --global user.name “Bilbo Baggins”
git config --global user.email “bilbo@shirerocks.com”
```

This will create a new ~/.gitconfig file that will look like this:

```
$ cat ~/.gitconfig
[user]
    name = Bilbo Baggins
    email = bilbo@shirerocks.com
```

# Getting a Git repository

## New repository

```
git init
```

This will create a .git directory in your current working directory that is entirely empty.

If you have existing files you want to add to your new repository, type:

```
git add .
git commit -m ‘my first commit’
```

## Cloning a repository

```
git clone git://github.com/justb/test_repo.git
```

If you want to put it in a different directory than the name of the project, you can specify that on the command line,
too.

```
git clone git://github.com/justb/test_repo.git myotherfolder
```

# Workflow

We can add patterns into the `.gitignore` file to tell Git that we don’t want it to track them. Example:

```
tmp/*
log/*
config/database.yml
config/environments/production.rb
```

A good way to find out what you’re about to commit (that is, what is in your index) is to use the status command.

```
$ git status
# On branch master
# Changed but not updated:
# (use “git add <file>...” to update what will be committed)
#
# modified: README
# modified: Rakefile
# modified: lib/simplegit.rb
#

no changes added to commit (use “git add” and/or “git commit -a”)
```

You could commit only the Rakefile:

```
git add Rakefile
git commit -m "Add new task"
```
![git commit and git add](img/gitaddcommit.png)

If we want to commit all our changes, we can use this shorthand:

```
$ git commit -a -m ‘committing all changes’
```
![git commit -a](img/gitcommita.png)