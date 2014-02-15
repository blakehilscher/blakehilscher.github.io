---
layout: post
title: "Show hidden files and folders in textmate."
date: 2012-10-04 21:14:48 -0500
comments: true
categories: snippets textmate
---

```ruby
# Want to show hidden files and folders in your TextMate project drawer? Simple, just modify the file and folder patterns in TextMate's preferences.
 
# Instructions:
# Go to TextMate > Preferences...
# Click Advanced
# Select Folder References
 
# Replace the following:
 
# File Pattern
!(/\.(?!\W*)[^/]*|\.(gitkeep|DS_Store|tmproj|o|pyc)|/Icon\r|/svn-commit(\.[2-9])?\.tmp)$
 
# Folder Pattern
!.*/(.git|CVS|_darcs|_MTN|\{arch\}|blib|.*~\.nib|.*\.(framework|app|pbproj|pbxproj|xcode(proj)?|bundle))$
```