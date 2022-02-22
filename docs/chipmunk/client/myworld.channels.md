---
title: myworld.channels
parent: Client Modules
grand_parent: Scripting
nav_order: 1
---
# myworld.channels
This module exposes channel communications to scripts. Channels are
used for chat, and may in the future be used for script-script
communication as well. Messages are sent on named channels, and
are received by listeners registered to those channels.

> Note that scripts currently can send to channels, but currently
> cannot receive from them.

## Variables
* `MAIN_CHANNEL` - the main channel name. Contains the value `main`.

## Methods
* `send(channel, msg)` - sends a message on the given channel
  * `channel` - String, the channel name
  * `msg` - Object, the message to send


* `say(msg)` - sends a message on the main channel
  * `msg` - Object, the message to send
