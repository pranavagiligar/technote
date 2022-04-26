---
title: "Amend your git author tag of one or more commits sequentially"
date: 2022-03-03T02:26:33+05:30
tags: ["git"]
draft: false
---

Change future commit author's tag with git global config as shown below

```bash
git config --global user.name "name_you_want_to_change"
git config --global user.email "email@you.want.to.change"
```

Now assume you have 3 commits `7743a3(HEAD) -> 52da64 -> 194150`, and you want to change author tag of `52da64` and `7743a3`, then execute below git command


```bash
git rebase -i 7743a3 -x "git commit --amend --reset-author -CHEAD"
```

If in case you want to reset author's tag from initial commit/ all commits, execute following command

```bash
git rebase -i --root -x "git commit --amend --reset-author -CHEAD"
```

After this force push your changes since you have modifed the commit and its hash. Following is the command assuming remote branch name is `master`

```bash
git push -f origin master
```

[Credit](https://www.deployhq.com/git/faqs/update-author-committer-multiple-git-commits)