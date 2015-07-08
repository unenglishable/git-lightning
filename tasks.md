#tasks!

##make a github account

https://github.com/join

##fork my repo for your team and clone it individually

1. Fork my repo: `https://github.com/unenglishable/git-lightning`
  - Press the fork button
  - Only one person has to do this

2. Set up permissions (add teammates as collaborators)

3. Clone the repo: `git clone git@github.com:username/git-lightning`

##make a directory in there with your team name (or username)

1. `mkdir team_name`

All your team's code will go in here.

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
    1. Take in user input
    2. Convert to upper case
    3. Write/output to the console
  - Stub a file.  Create a new file with a comment that contains your team's
    name.
  - Commit and push that file
  - Have everyone do `git pull` get the latest changes
  - Split up these tasks amongst your team
    - Each member should be doing the task on their own instance of a repo.
    - When you are done with the task, commit it like before, but do not push
      yet.
    - Each version of the code file should do exactly one thing.

3. hello world again (merge conflicts)
  - Take your hello world program and edit it to say "Hello World, again."
  - Split this task up into parts
    - Capitalize
    - Add punctuation
    - Add "again"
  - Since you are changing the same line, this will result in a merge conflict

