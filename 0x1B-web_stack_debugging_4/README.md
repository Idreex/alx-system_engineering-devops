# Web stack debugging #4

This was the fifth in a series of web stack debugging projects. In these
projects, I was given broken/bugged webstacks in isolated containers,
and tasked with fixing the web stack to a working state. For each
task, I wrote a script automating the commands necessary to fix the
web stack.

## Tasks :page_with_curl:

* **0. Sky is the limit, let's bring that limit higher**
  * [0-the_sky_is_the_limit_not.pp](./0-the_sky_is_the_limit_not.pp): Puppet manifest
  that increases the amount of traffic an Apache web server can effectively handle.

* **1. User limit**
  * [1-user_limit.pp](./1-user_limit.pp): Puppet manifest that changes the operating system
  configuration so that it is possible to login with the user `holberton` and open a file
  without error.

