# Hush


## Problem

Computers provide people with two main functions. They store content, and they allow its manipulation. Manipulation capabilities are typically bundled in applications, but this paradigm has limits because it locks actions to a fixed set of features. Expert users often have to switch among different applications to get their work done. Command line tools provide more fine grained access to functionality, but offer poor guidance and discovery. As a result, users are often limited in performing actions directly on their content. This problem increases as content and activities are distributed across non-pc computers such as smartphones.

## Approach

Hush is an attempt to make any conceptually meaningful action available to users in any context, across devices. It consists of four parts.

* A local web server that exposes the computer's file system over HTTP.
* A local web server that wraps command line tools applicable to content into web services.
* A registry that defines what actions can be executed on which type of content. This includes metadata and semantics of how to use the service and which arguments to supply. It also describes how high-level goals map to individual actions, and how the UI must guide the user.
* A UI that displays content and dynamically deduces which actions are available to it in the current context. It can execute local and global web services on content.

## Implementation

Technically, the system is implemented on top of an existing Linux distribution, using a node.js server to expose services, and a browser based HTML5 user interface. The proof-of-concept prototype should allow the user to:

 - browse the file system
 - edit text files
 - rotate & apply filters to images
 - share a wired internet connection on an ad-hoc WLAN

