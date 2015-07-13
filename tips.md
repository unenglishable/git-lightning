#Protips

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
```
*.o
*.out
node_modules/
temp/
```

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
