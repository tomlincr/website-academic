---
title: Implementing wget in Jupyter Notebooks on Windows 10
date: 2021-04-14
draft: false
featured: false
authors:
  - admin
tags:
  - python
  - jupyter
  - windows
  - linux
image:
  filename: ""
  focal_point: ""
  preview_only: false
---
🚩 Problem: Trying to use `wget` from within Jupyter Notebooks on Windows

❓ `wget` is a free useful tool for downloading files (web-get) that is typically bundled with Unix-based operating systems like Linux & MacOS, but not Windows.

💡 [Eternally Bored](https://eternallybored.org/misc/wget/) produce compiled Windows binaries of [GNU Wget (only 32-bit)](https://www.gnu.org/software/wget/).

🔧 After downloading, move `wget.exe` into PATH (typically `C:\Windows\System32`, but can be found by entering `path` into the Windows Terminal/Command Prompt).

💻 You can then call it via Jupyter using `!` to access terminal commands, e.g.

`!wget http://www.gatsby.ucl.ac.uk/teaching/courses/ml1/binarydigits.txt` ✅
