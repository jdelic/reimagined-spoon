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

So when in doubt, always choose an asynchronous way of communicating, unless
you need to communicate something really urgent. That's how Slack becomes a
really useful tool.

What do you mean by "asynchronous" anyway?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
In this case "asynchronous" means two things:
 1. "not immediate" and
 2. "under the receivers control".

Examples synchronous communication
 * Phone call
 * Walking over to your desk
 * Walking into your office
 * Shouting across the room

Examples for asynchronous communication
 * Chat tools
 * Email
 * Ticket system
 * A post-it left on a desk

Unlike when you walk up to my desk, with a chat tool I get to *choose when to
process your message*. I also get to choose myself when I want to be part of
a conversation inside a channel or just read up on what happened later or
ignore the conversation outright. On the other hand, I am also responsible for
making sure that I am part of the channels and conversations that I want to
follow and configuring my notification options so I only get interrupted by
things that are important to me.

You can use Slack to send someone messages in such a way that they are
alerted to them (in Slack you do this by putting an '@' in front of their
name), but even then, you shouldn't expect anyone to just drop what they're
doing and answer you. The idea of a chat tool is that people can tune in and
out of a conversation and respond to messages when it's convenient for them and
even when you ping them directly, they ideally are able to finish a task before
answering, letting them structure their time more efficiently, while still
providing everyone with a way of communication that is less formal and more
efficient than an email.

To summarize
~~~~~~~~~~~~
Your responsibility is to make sure that Slack complements and supports your
work by making sure that your notification settings and channel settings and
your "away" and "do not disturb" settings are configured optimally.

Everybody else's responsibility is to not abuse the privilege of being able to
interrupt you in your work.


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
* But generally, it's much better to discuss most things openly, but in such a
  way that it also doesn't disrupt other peoples' conversations.
* So open a separate Slack channel, open a ticket or create a collaborative
  mindmap or wiki page and pull in the people needed to work on it, but make
  the *process*, the *discussion* and *its result* widely available by default.

This means avoiding private one-on-one chats unless you are discussing
something really private. If it's just something that "might not interest
everybody in this channel" and if it's going to be a longer conversation, just
move the discussion to its own channel, this way you still give people a chance
to participate, just like when you meet at the coffee machine and talk about
something in earshot of other people.


Slack channels are cheap
------------------------
**When in doubt, open a channel.**

We run `destalinator`_. This is a bot that will reap unused Slack channels and
keep everything tidy and clean up after you. On the other hand that means that
we can open Slack channels for everything and use them as long as we need them
and it makes sense to keep them. After that they will disappear magically. So
never worry about opening a Slack channel too many.

Allow people to self-organize
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Especially as managers we often try to anticipate the "ideal pattern" for
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


Avoid naked pings!
------------------
`Nobody likes naked pings`_ lists a whole list of articles about why those are
harmful. But I'm going to sum up the argument here:

**Don't send messages to people saying just "Are you there?" or "do you have a
moment?" or "can you call me?"**

Those are called "naked pings". Non-actionable calls to action. The missing
part is context: i.e. "why do you need me?", "what do you want to talk about?",
"what can I help you with?". Instead try and let people know what you need
from them when you contact them. As mentioned above,

1. this allows them to use their own time efficiently and judge whether they
   can reply to your request right away or rather finish something up first and
2. it removes the inherent passive-aggressiveness of asking someone to do
   something without telling them why.

So instead be a good chat neighbor and say: "Hey, can we have a short call? I'm
struggling with your code in module X, I can't figure out how it does Y."


.. _Joel Spolsky:
.. _joelonsoftware: https://www.joelonsoftware.com/
.. _Private Offices Redux:
    https://www.joelonsoftware.com/2006/07/30/private-offices-redux/
.. _When the walls come down:
    http://www.oxfordeconomics.com/when-the-walls-come-down
.. _destalinator: https://github.com/randsleadershipslack/destalinator
.. _Nobody likes naked pings:
    https://blog.doismellburning.co.uk/nobody-likes-naked-pings/
