---
layout: post
title: Nicer git log
category: [Development]
tags: [dev,bash]
---

Just a short one. I want to share a simple command to display nicer `git log` in the terminal. `git log` has `--pretty=format` option built-in, we are just going to pass formatting to it.

```
git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'
```

And it looks like this:

{:.Image.Image--lg}
![Nicer git log](/public/img/nicer-git-log.png)

Then add it to your `.bash_profile` as an alias (I'm using `glog`) and that's it.

```
alias glog="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'"
```
