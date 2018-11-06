1) `git remote` lists all remote branches
2) suppose i have a local repo. and i want to start publishing it to remote repo on github. first, i need to connect them with `git remote add origin <remote repo address>`
3) `git push <remote short name> <branch>` sends commits to a remote repo
4) to sync our local copy of the repo with the original remote repo we use `git pull <remote short name> <branch we want to pull from>`
5) `git pull origin master` = `git fetch origin master` && `git merge origin/master`
6) *Forking* in terms of github means creating an identical copy of repo.
7) `git shortlog` shows how many contributor made commits `-s` option shows number of commits, `-n` option sorts the output
8) `git log --author=<Author name>` shows commits made by a user with specified name
9) `git show --grep=<regex to search>` display only commits which show
10) `origin` vs `upstream`: i forked a repo. `origin` is a remote of my fork, where `upstream` is an origin of the *original repo i forked*.
11) I've made three commits which were minor changes. I can `squash` them into one commit using `git rebase`.
12) `git rebase -i HEAD~<number of commits to squash>` will
    1) Take `<number of commits>` starting from the most recent one in the head;
    2) Squash them into new commit;
    3) Moves master to point at this new commit;
    4) **Save commits of the squash into backup branch**.
13) `-i` flag means `interactive` i.e. i am guided through the stages of rebase step by step.