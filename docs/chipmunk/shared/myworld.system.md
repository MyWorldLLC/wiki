---
title: myworld.system
parent: Shared Modules
grand_parent: Scripting
nav_order: 1
---
# myworld.system
This module exposes basic system variables and functions.

## Variables
* `args` - immutable list of arguments supplied to the script at
  launch time. The arguments may be of any type, including objects.
* `env` - immutable map of environment variables. Keys are strings,
  values may be of any type, including objects.

## Methods
* `exit()` - causes the script to immediately exit with a `null` exit value.
* `exit(exitValue)` - causes the script to immediately exit with the given
  exit value.
