---
title: "Thoughts on Bash"
date: 2022-08-10T16:23:40-06:00
draft: false
---

Just reworked my website in Hugo, like the new look? --

Anyway, here's a quick post to show off the new site.

I was listening to _The Lex Fridman_ podcast, as one does. And he asks everybody "what's your favorite programming language?". First off, as if that's important. Secondly, many guests have pretty good answers.

Mine would be `bash`. Because, the purpose of a programming language is to serve as a bridge between the human brain and a CPU. Bash is basically the same when it's hand typed (i.e. giving commands through a terminal emulator) as when it's scripted. Therefore, one might be inclined to think, that it lives in a happy medium between _wetware_ and _hardware_.

I could even go into how bash evaluates the same variables as numeric or string without having to cast. Take: 

```bash
$ a=2
$ echo "$a + 1"
2 + 1

$ echo "$(($a + 1))"
3
```
Pretty similar to how a human interprets numbers written on a whiteboard? Food for thought.


Until next time reader,

Oriwarth

{{<centerImg src="/img/3_Knight.png" mouse="Knight 3" scale="200vw">}}

