---
title: Interface Guidelines
copyrights:
  -
    name: "Ryan Heywood"
    email: "ryan@hashbang.sh"
---

# Interface Guidelines

IRC was designed in a time where programs worked on a mostly text based
interface and shipped wiht a manual. Since then, various other forms of
communication showed up which were commonly judged as "better" than IRC because
the clients were more intuitive. Most IRC clients offer IRC functionality on a
level similar to the protocol itself, using client "commands" in a fashion
similar to the verbs of the protocol itself - a common case being the "msg"
command, `/msg <nick> <message>`, which becomes `PRIVMSG <nick> :<message>`.

While this format works for users who are used to that interface, it might not
be intuitive for people who prefer a graphical interface. Context menus, like
ones activated by right-clicking on elements, can be a very useful way of
managing users in a channel (granting someone a status, kicking, banning, or
even effects outside of the channel such as opening a messaging window). This
is common with websites and graphical applications and can make IRC clients
feel much more intuitive and much more like a "modern" application.

To establish this feel, it might be useful to develop a client with both of
these formats in mind. In a development mode, it might be useful to turn off
all slash-command components of a client and rely solely on the graphical
components of your application to use IRC nearly as efficiently as you would
otherwise. The same should also be done with a command-based interface, to
catch some things that aren't specific to the protocol but might relate to your
client; WeeChat, for example, has the `/buffer` subcommand which is not at all
related to the IRC protocol but allows for controlling buffers (i.e. spaces
containing text; channels, servers, messages, and the like) without using your
mouse at all.

Now, your client should now be accessible to people who are inclined to use a
mouse rather than the keyboard, and similarly to people who are inclined to use
the keyboard rather than the mouse. However, if the graphical framework for the
client supports it, it might also be useful to allow for voice controls to help
with people who can't see as well as most users. This could be done by giving
labels to a voice-control tool through labels given to graphical components.
