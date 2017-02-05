---
layout: post
title:  Emacs C-SPACE problem on Bash-win10
date:   2017-2-5 11:12:00 +0800
categories: articles
---

## Can not be solved
In bash terminal on windows 10, emacs mark set command , C-space wont work. It seems some bugs in UBUNTU. C-space, C-@ produce nothing so Emacs can't recognize it.

According an article on Reddit, type "showkey" in the terminal to test the coding of keyboard typing combination. It's true.

So my solution is to add another empty key binding to set-mark-command in my .emacs file:

(global-set-key (kbd "M-c") 'set-mark-command)

Done!







