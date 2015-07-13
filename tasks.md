#tasks!

##make a github account

https://github.com/join

##make a directory in there

1. `mkdir [some_name]`

2. `cd [some_name]`

3. `git init`

All your code will go in here.

##start writing some code

Using any language you want, complete the following tasks.

1. hello world (practice committing)
  - The program should output: "hello world"
  - You can check what files have changed with `git status`
  - When you are done, do `git add [file]`
  - Check again with `git status` to make sure you have added the correct file.
  - Do `git commit` when you have staged the correct files.  Otherwise do `git
    reset [file]` on files you do not want to commit.
  - Write a commit message.
  - Make sure you are on your team's branch `git branch`
    - This command should show a * next to your current branch.
  - Push your code to github `git push`

2. uppercaser (practice adding to a file)
  - The program should take in user input and output the uppercased form of the
    text.
  - Breaking the program down into steps we have:
    1. Take in user input and output to the console.
    2. Convert to upper case
  - Stub a file.  Create a new file with a comment that contains a comment with
    your team's name.
  - Commit and push that file
  - Have everyone do `git pull` get the latest changes
  - Split up these tasks amongst your team
    - Each member should be doing the task on their own instance of a repo.
    - When you are done with the task, commit it like before, but do not push
      yet.
    - Each version of the code file should complete one step.

3. hello world again (merge conflicts)
  - Take your hello world program and edit it to say "Hello World, again."
  - Split this task up into parts
    - Capitalize
    - Add punctuation
    - Add "again"
  - Since you are changing the same line, this will result in a merge conflict
    resolve the merge conflict.
