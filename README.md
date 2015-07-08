#git lightning start!

##first time git stuff

*. Create ssh key (or add it to github if you already have one)
  - `mkdir ~/.ssh`
  - `ssh-keygen`, and follow the directions
  - choose a directory like `~/.ssh/id_rsa`

1. `git config --global user.name "your name"`

2. `git config --global user.email your@e.mail`

3. rerere

http://psung.blogspot.com/2011/02/reducing-merge-headaches-git-meets.html

4. merge conflict style diff3


------DONT DO THIS
##new git project

1. create a directory

2. `git init`

3. add `README.md`

4. add `.gitignore`

5. create and name github repo

6. add the remote and push

ie: `git remote add origin git@github.com:user/repo-name`
------DONT DO THIS

##get a github project

1. find the repo on github

2. look for the ssh clone link

3. `git clone [link]`

eg: `git clone git@github.com:unenglishable/git-lightning`
