1) Revision history isn't that flexible and misses few options:
    - the ability to label a change;
    - the ability to give a detailed explanation of why a change was made;
    - the ability to move between different versions of the same document;
    - the ability to undo change A, make edit B, then get back change A without affecting edit B.
2) Cheatsheet:
    - Repository / repo
    A repository is a directory which contains your project work, as well as a few files (hidden by default on Mac OS X) which are used to communicate with Git. Repositories can exist either locally on your computer or as a remote copy on another computer. A repository is made up of commits.

    - Working Directory
    The Working Directory is the files that you see in your computer's file system. When you open your project files up on a code editor, you're working with files in the Working Directory.
    This is in contrast to the files that have been saved (in commits!) in the repository.
    When working with Git, the Working Directory is also different from the command line's concept of the current working directory which is the directory that your shell is "looking at" right now.

    - Checkout
    A checkout is when content in the repository has been copied to the Working Directory.

    - Staging Area / Staging Index / Index
    A file in the Git directory that stores information about what will go into your next commit. You can think of the staging area as a prep table where Git will take the next commit. Files on the Staging Index are poised to be added to the repository.

    - SHA
    A SHA is basically an ID number for each commit. Here's what a commit's SHA might look like: e2adf8ae3e2e4ed40add75cc44cf9d0a869afeb6.

    It is a 40-character string composed of characters (0–9 and a–f) and calculated based on the contents of a file or directory structure in Git. "SHA" is shorthand for "Secure Hash Algorithm". If you're interested in learning about hashes, check out our Intro to Computer Science course.

    - Branch
    A branch is when a new line of development is created that  diverges from the main line of development. This alternative line of development can continue without altering the main line.
    Going back to the example of save point in a game, you can think of a branch as where you make a save point in your game and then decide to try out a risky move in the game. If the risky move doesn't pan out, then you can just go back to the save point. The key thing that makes branches incredibly powerful is that you can make save points on one branch, and then switch to a different branch and make save points there, too.

3) `git clone <repo_url> <dir_name>` will clone a repo from specified url in a specified dir
4) `git log --oneline` is a good command to see repo's overview
5) `git log --stat` is a handy command that shows not only commits but there stats as well
6) `git log -p` shows detailed log
7) `git show <commit id>` shows particular commit info
8)  `git tag -a v1.0` adds a tag with a `v1.0` label
9) `git tag -d <tag_name>` deletes a tag with the specfied name
10) `git tag -a <tagname> <commit_sha>` will attach a `tagname` to a commit with sha `commit sha`
11) `git branch alt-sidebar-loc 42a69f` will create `alt-sidebar-loc` branch which will point the commit with SHA `42a69f`
12) `git log --oneline --decorate --graph --all` will show a simple graphic representation of `all` branches of the repo
13) `git commit --ammend` alters the latest commit
14) `git reset`
    - `--mixed` (default) moves files to wd
    - `--soft` to staging
    - `--hard` erases
15) 