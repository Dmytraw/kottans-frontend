# kottans-frontend

## Lesson 1: what i learned aboot version control system GIT
General purpose of VCSs are designed to store main milestones of development and to make collaboration between developers more easy through branching and history in particular.
### What i learned from Udacity lessons:
0) Operating systems have built-in tools to compare files (`fc` for windows and `diff` for macos/linux)
1) I hate typos. Small typos (like an `i` instead of `l` in a word) are the worst because u cannot spot them quickly with your eyesight. But diff helps to spot not only these small parasites, but also bigger pieces of code.
2) History of file changes could help to see what went wrong in a certain period of time and also how to make things written long time ago better.
3) It's good to have manual saves (commits) because it helps to make save only when logical piece of the project was implemented. It keeps the  history of the project more clean.
4) Storing multiple files in one commit might point that they are related.
5) `git config --global color.ui auto` is a handy command to see color-friendly outputs of the `git diff` command.
6) `git diff <commit_id> <commit_id>` ran with `--stat` argument can show how many files were added and deleted.
7) `git log` shows all the commits made on the certain branch