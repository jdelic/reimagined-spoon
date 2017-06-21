Asynchronous communication
==========================

People use every communication tool differently everywhere and like
every CTO/Head of <anything>/Team lead, I have my own thoughts about what
constitutes effective use. This document contains those thoughts.


Asynchronous communication is a quick win for any IT organization
-----------------------------------------------------------------
It seems to be widely ignored, but for years now, scientifically there have
been indications that open plan offices are *not* facilitating positive
communication, good practices or better knowledge sharing, or at least only at
the cost of serious drawbacks. For more context, you can refer to:

* `When the walls come down`_
* `Why we still believe in private offices <Private Offices Redux_>`_
* The book Peopleware by Tom DeMarco and Timothy Lister
* Everything that `Joel Spolsky`_
  `has written on the topic <Private Offices Redux_>`_ (and really any other
  topic as well)

Instead, we can safely say, that every synchronous communication
interaction also incurs a huge cost. In my mind, there are only two roles when
I interrupt what you are doing at your desk: perpetrator and victim.

=========================    ============================
Synchronous communication    Asynchronous communication
=========================    ============================
Phone call                   Chat tools
Walking over to your desk    Email
Walking into your office     Ticket system
Shouting across the room     A post-it left on your desk
=========================    ============================

So when in doubt, always choose an asynchronous way of communicating, unless
you need to communicate something urgent. That's where Slack becomes a really
useful tool.


"Fail Open"
-----------
**"If you have no explicit obligation or reason to keep something to yourself,
choose the best available asynchronous, non-disruptive communication method
available that allows the most people to participate if they want to or
inform themselves after the fact."**

Let's unpack the above statement:

* Obviously some things in a company need to be kept secret. Some information
  is protected by law (employment information, customer information, etc.) and
  some information is volatile to the company (revenue information,
  employee performance).
* But generally, it's much better to discuss anything openly, but in such a way
  that it also doesn't disrupt other peoples' work.
* So in that case, open a Slack channel, open a ticket, create a collaborative
  mindmap or wiki page and pull in the people needed to work on it, but make
  the *process*, the *discussion* and *its result* widely available.


Slack channels are cheap
------------------------
**When in doubt, open a channel.**

We run `destalinator`_. This is a bot that will reap unused Slack channels and
keep everything tidy and clean up after you. On the other hand that means that
we can open Slack channels for everything and use them as long as we need them
and it makes sense to keep them. After that they will disappear magically. So
never worry about opening a Slack channel too many.

Walk treaded paths
~~~~~~~~~~~~~~~~~~
Especially as managers ee often try to anticipate the "ideal pattern" for
communication and often that pattern needs to reflect certain business
realities. For example, the structure of JIRA projects and what source code
goes into what repositories creates dependencies that are hard to change later
and so "designing" them beforehand makes good sense.

However, I don't feel that the same is true for structures that are as easy to
change like the channel structure on a chat server. As I already mentioned,
*channels are cheap*. So I don't think that we should enforce any particular
channel structure. Instead, trust people to self-organize into efficient
groups and do the same for your own work. Don't fear being part of many, many,
channels! Use Slack's per-conversation notification settings and powerful
configuration options to ensure that you're part of the conversations that are
useful for you without impacting other peoples' options to communicate with
each other.


.. _Joel Spolsky:
.. _joelonsoftware: https://www.joelonsoftware.com/
.. _Private Offices Redux:
    https://www.joelonsoftware.com/2006/07/30/private-offices-redux/
.. _When the walls come down:
    http://www.oxfordeconomics.com/when-the-walls-come-down
.. _destalinator: https://github.com/randsleadershipslack/destalinator
