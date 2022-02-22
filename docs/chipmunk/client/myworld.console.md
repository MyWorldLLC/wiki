---
title: myworld.console
parent: Client Modules
grand_parent: Scripting
nav_order: 1
---
# myworld.console
This module allows scripts to print to the client console. Console
messages will appear in two places: chat windows that have not disabled
system messages and the client's standard out stream, where they will be
visible if the client is running from a terminal (which will typically 
only be in development environments). Console messages in the chat window
are notated with a `System:` label.

## Methods
* `print(msg)` - prints a message to the client's system console
    * `msg` - Object, the message to display