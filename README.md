# C++ Fundamentals Course, SoftUni, March-April 2022 #

[SoftUni-Break](https://softuni-break.github.io/)

## What is this ##

This repo contains my files for C++ Fundamentals course for SoftUni, March-April 2022.

## How-to Articles ##

### Setting up your development environment for C++ ###

Since Visual Studio does not (yet) support C++ development on Mac M1, we need to setup another development environment. For this course, a simple C++ compiler, with a library and a make system should do.

There are many articles on the net how to do this. I recommend using plain-old [C++ Installation on MacBook M1 for VS Code](https://www.geeksforgeeks.org/c-installation-on-macbook-m1-for-vs-code/).

There are other articles there too, like [How to create the boilerplate code in VS Code?](https://www.geeksforgeeks.org/how-to-create-the-boilerplate-code-in-vs-code/).

And, of course, there's THE tutorial from Microsoft [Using Clang in Visual Studio Code](https://code.visualstudio.com/docs/cpp/config-clang-mac), which guides you how to configure it all.

### Fixing default Debug extension for M1 ###

It turns out, the default debug extension for VS Code still does not work on M1 chips. After doing all by the book, it drove me crazy that when I start debugging, it would wait for a few seconds, and then kill the program without doing nothing.

After enabling extensive logging (`"logging": { "engineLogging": true, "trace": true, "traceResponse": true }`), I [found](https://www.google.com/search?q=%22Unable+to+start+debugging.+Unexpected+LLDB+output+from+command+%22-exec-run%22%22&sxsrf=APq-WBs_C4jXXLEN9ore6Z9Y4dRRLWU14g%3A1644741309682&ei=vcIIYqmfKcaVxc8PzJ2c4A0&ved=0ahUKEwjp8Yrsovz1AhXGSvEDHcwOB9wQ4dUDCA4&uact=5&oq=%22Unable+to+start+debugging.+Unexpected+LLDB+output+from+command+%22-exec-run%22%22&gs_lcp=Cgdnd3Mtd2l6EAMyBggAEBYQHjIGCAAQFhAeMgYIABAWEB46BwgAEEcQsANKBAhBGABKBAhGGABQ9AVYuwxgsRZoA3ABeACAAYQBiAHMApIBAzEuMpgBAKABAaABAsgBCMABAQ&sclient=gws-wiz) out [the error](https://github.com/microsoft/vscode-cpptools/issues/6779). Once there, the solution was [just an extension installation away](https://github.com/microsoft/vscode-cpptools/issues/6779#issuecomment-854675319).

### dreampuf/GraphvizOnline tool for drawing diagrams ###

[The Graphviz tool](http://www.graphviz.org/)[(online)](https://dreampuf.github.io/GraphvizOnline/) is a diagraming tool, which you can easily program in an YAML-like language. You create your diagram in this language, and the tool draws for you the result. It could be plain (in the beginning, at least), but it does the job right, and it helps you quickly draft a diagram of almost any kind.

The tool also has [a desktop app](http://www.graphviz.org/download/), and [an online service](https://dreampuf.github.io/GraphvizOnline/), which does pretty much the same (quick and dirty). It seems it has a complex customization language, descibed in [its documentation](http://www.graphviz.org/documentation/)[\[pdf\]](http://www.graphviz.org/pdf/dot.1.pdf).

I need to bookmark this and start using it more!
