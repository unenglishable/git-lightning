#Protips

##Command line Git log

In your `~/.aliases` file:

`alias gl="git log --graph --abbrev-commit --pretty=oneline --decorate"`

With this alias, `gl` shows you the commit tree, similar to `gitk`.  If you
don't have a Git GUI, this command is absolutely necessary.  You can use the
`--all` argument to see all branches.

`gl --all`

See [interactive rebase](###Interactive Rebase) for more help on viewing commit
history in the command line.

##Commit messages

There are several conventions that will help you make the most use out of commit
messages.

###Subject line

This line should be 70 characters or less, and be written in present-tense.
This is to show what change the commit accomplishes rather than what you did.
It might not be apparent at first, but it makes sense when looking back at the
changes that were made by the entire team.

###Message body

This is a description of what you did, why you needed to do it (what issues were
tackled), and how you provided a solution.  When looking back at old changes, it
is beneficial to have a log of this information because it is easy to forget how
a problem was solved before.  In addition, leaving a detailed commit message
will help others understand the changes that you made.

##.gitignore

This file tells Git not to track changes on certain files and directories.  It
keeps your repository smaller and more organized by not including files that can
be automatically generated.

When working on a large project with lots of automatic configurations, .o files,
generated logs etc., include these in the `.gitignore`.  You can include them by
editing the `.gitignore` file in the top directory of your project - one file or
directory per line.

To add a certain file extension, use the wildcard `*`.
To add a directory, just type that directory's name. You can leave a `/` at the
end of a name in the `.gitignore` to remind you that it is a directory.
Git will parse the `.gitignore` file the same way you would navigate in the
command line.

Example `.gitignore`:
````
*.o
*.out
node_modules/
temp/
````

##Merge conflicts

Merge conflicts happen when two commits have changed the same line, or add the
same lines.

Dealing with merge conflicts can be one of the most frustrating tasks when
learning git.  When you get a merge conflict, it's important to understand what
you are looking at in a conflicted file.

In the default mode, there are two parts:

`<<<<<<< HEAD`

`>>>>>>> [other-branch]`

These parts are separated by:

`=======`

The code in HEAD is the code that has been written in the current branch.  The
code in [other-branch] are the changes you are trying to merge in.  By enabling
`diff3`, you can also see the common ancestors of the two branches.

[read about diff3 and
rerere](http://psung.blogspot.com/2011/02/reducing-merge-headaches-git-meets.html)

##Patch add/reset/checkout

`git [add/reset/checkout] -p`

Adding code with a patch useful for committing specific lines in a file.  This
helps keep your commits logically separate, which plays a big role in how useful
git will be in your project.  Developers have different ideas about how much
code is acceptable to have in each commit.

Over time, you may find that your commits are too large to easily pick and choose
lines of code from.  I've gotten used to making tiny commits, with just enough
code to complete a small task or a single part of a large task.

##Rebase

`git rebase [branch]` OR `git rebase [base] [branch]`

This command rebases your current branch onto `[branch]`.  It will take whatever
commits that are new on your branch and try to stack them onto the end of the
other `[branch]`.  Rebasing is good for adding changes from another branch into
your current working branch.  (if your workflow involves working on a branch
locally)

Be careful when using this with a team.  If you rebase a branch that you have
already pushed, it requires a force push (`git push --force`) to update the
remote branch.  I highly recommend avoiding `--force` on a push.  It is VERY
inconsiderate to other people working on your project.  Use the interactive
rebase on a branch that you have not pushed yet, and use a `git merge --no-ff`
on a branch that you have already pushed.

###Interactive Rebase

`git rebase [branch] -i`

The interactive rebase is helpful for editing your current commit tree.
