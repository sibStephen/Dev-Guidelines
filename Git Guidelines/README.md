# Git Guidelines

## Common Guide
- When you are pulling code, prefer `rebase` over `merge`. `git merge` creates
merge bubbles and it makes the history confusing.

#### Cons of `git merge`
- Makes repo history confusing and noisy.
- Duplicate code in commits. You are debugging using `git blame`, the same code
will appear twice in history, one in the actual commit and the other in merged
commit.

#### Doing Git rebase by default
- Force all new branches to automatically use rebase `git config --global branch.autosetuprebase always`
- Force existing branches to use rebase `git config branch.*branch-name*.rebase`

**Sources**
- Steve Harman's blog _Git Pull With Automatic Rebase_ http://stevenharman.net/git-pull-with-automatic-rebase
