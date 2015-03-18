Go binding of C Telegram library
================================

This is a WIP integration of C Telegram library (https://github.com/vysheng/tgl) into Go

[![Build Status](https://travis-ci.org/gloob/go-telegram.svg?branch=master)](https://travis-ci.org/gloob/go-telegram)
[![Join the chat at https://gitter.im/gloob/go-telegram](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/gloob/go-telegram?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Version: 0.1-alpha

Documentation: http://godoc.org/github.com/gloob/go-telegram/tgl

LICENSE
-------

go-telegram is licensed under the Apache License, Version 2.0 (http://www.apache.org/licenses/LICENSE-2.0.html).

Current Development Status
--------------------------

* Alpha version
 * In planning phase.
 * ~~Any useful code yet.~~
 * Exposing the library into Go without any aliasing.

***

* Beta version
 * TbD

How to Install
--------------

Sadly we are facing two problems with the current project approach:

1. Unsupported git submodules in go get command. (https://github.com/golang/go/issues/7764)
2. Currently tgl library doesn't have a pkg-config package defined, so we need to compile it by ourselves in the correct location. (TODO: Need to create a issue for this or provide a pull request to the tgl project)

So you need to do some manual arrangment to succesfully install the package.

```
    $ go get -d github.com/gloob/go-telegram && \
      cd $GOPATH/src/github.com/gloob/go-telegram && \
      git submodule update --init --recursive && \
      cd ./lib/tgl && ./configure && make && \
      go get -u github.com/gloob/go-telegram
```

TODO:

* Refactor Makefile with the previous problems to automatically create using make.
* Check viability of using subtree instead of submodules (http://blogs.atlassian.com/2013/05/alternatives-to-git-submodule-git-subtree/)
* Create issue to check viability to add pkg-config support to tlg.

Current Status
--------------

 * Linux
   * Not yet!
 * Mac OS
   * Not yet!
 * Windows
   * planned for 2015 Q4

Sample Program
--------------

Check ./examples directory. (WIP)

You can contact me at gloob@litio.org
