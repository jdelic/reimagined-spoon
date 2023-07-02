Asynchronous communication
==========================

People use every communication tool differently everywhere and like
every CTO, I have my own thoughts about what constitutes effective use. This
document contains those thoughts.


Asynchronous communication is a quick win for any IT organization
-----------------------------------------------------------------
It seems to be widely ignored, but for years now, scientifically there have
been indications that open-plan offices are *not* facilitating positive
communication, good practices or better knowledge sharing, or at least only at
the cost of serious drawbacks. For more context, you can refer to:

* `The Truth About Open Offices <HBR_Open_Offices_>`__
* `When the walls come down`_
* `Why we still believe in private offices <Private Offices Redux_>`_
* The book Peopleware by Tom DeMarco and Timothy Lister
* Everything that `Joel Spolsky`_
  `has written on the topic <Private Offices Redux_>`_

Regardless of what type of office you work in, I think we can safely deduce
that every synchronous communication interaction at least incurs some cost.
That's how I arrived at the conclusion that there are only two roles when
I interrupt what you are doing at your desk: perpetrator and victim.

So when in doubt, always choose an asynchronous way of communicating, unless
you need to communicate something really urgent. That's how a company chat tool
like Slack becomes a really useful tool.


What do you mean by "asynchronous" anyway?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
In this case "asynchronous" means two things:
 1. "not immediate" and
 2. "under the receivers control".

Examples for synchronous communication methods
 * Phone/Skype/Whatsapp/Teams/Zoom/etc. call
 * Walking over to your desk or into your office
 * Shouting across the room

Examples for asynchronous communication methods
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
things that are important to me or you.

You can use Slack to send someone messages in such a way that they are
alerted to them (in Slack you do this by putting a '@' in front of their
name), but even then, you shouldn't expect anyone to just drop what they're
doing and answer you. The idea of a chat tool is that people can tune in and
out of a conversation and respond to messages when it's convenient for them and
even when you ping them directly, they ideally are able to finish a task before
answering, letting them structure their time more efficiently, while still
providing everyone with a way of communication that is less formal and more
efficient than an email.

Your responsibilities as a message receiver
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Your responsibility is to make sure that communication tools complement and 
support your work by making sure that your notification settings and channel 
settings and your "away" and "do not disturb" settings are configured optimally.

This is not an excuse to have your notifications snoozed 24/7 or to just ignore
your team's channel. Instead, it's also your responsibility to communicate
effectively and respond to other people when you *are* available. Let them know
that you have seen their message, even by just adding a :+1: as a reaction.
Also let the channel know if you're doing something about the contents of a
message. This will avoid other people starting to do the same work.

If you regularly have to answer urgent emails, turn on email notifications.
Otherwise don't.

For example, I check my email 3 or 4 times per work-day or once every couple of 
days when on vacation. Unread notification badges are turned off for email. I 
have an autoresponder informing people to contact me via Slack and override my
notification snooze if their message is urgent.

Your responsibilities as a message sender
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
When sending a message, your responsibility is to not abuse the privilege of 
being able to interrupt others by overriding their notification settings. Use
terms of relative urgency in your message to ensure that the receiver knows what 
priority they should assign to your message.

When you override notification settings, explain why you did that. Somebody put
a "do not disturb" sign on their door and you ignored their wishes. You should
tell them why.

On the other hand, it's not your job to prevent the other person from receiving
your communication. If we all adhere to the rules laid out in this document, 
you should be able to send your email, your chat message, your asynchronous
communication at any time. It's the receiver's responsibility to ensure that
they are undisturbed by these messages when they want to be left alone for
whatever reason, like when they are on vacation. It's your job to not be
bothered by the asynchronicity of the interaction or deliberately impose a
synchronous method when necessary.

It's important to note that there is **one exception** to what I wrote above: the
above is only true if the receiver **can actually remove themselves from the
conversation or manage their notification settings**. In many companies there
are mailing lists that reach "all hands" or similar methods. They are important
as they allow company-wide (or team-wide, etc.) communication. However, in that
specific case, **it's on you as the sender** to really make sure that you are
using these methods only for appropriate communication that's useful to at
least a majority of the recipients. If you keep sending communications to a
mailing list that's only useful for a subset of a list, consider creating a new
subset of the list, or sending the communication through other means
altogether.

Your responsibilities as a manager in my orgchart
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Don't make asynchronous communication useless to people by demanding they treat
it like synchronous communication. 

If you need something urgently, use urgent communication methods. Make a
conscious decision about the cost that you are imposing on your victim. If you
send an email when someone is on vacation, as per above, that's ok. But if you
then insist that they check their phone every 10 minutes so they can reply to
your email, you have just multiplied the cost for everybody immensely, yourself
included. So don't do that. Think about what you are going to do, then override
their notification settings.


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

The solution to the above is almost never an email thread. Reading up on a
Slack conversation or thread you have been invited to after it had already
started, is infinitely better than reading through a nested email thread 
forwarded to you. Especially if your company insists on using an email client
like Outlook that for 20+ years hasn't learned basic features like nested
quoting.


Slack channels are cheap
------------------------
**When in doubt, open a channel.**

We run `destalinator`_. This is a bot that will reap unused Slack channels and
keep everything tidy and clean up after you. On the other hand that means that
we can open Slack channels for everything and use them as long as we need them
and it makes sense to keep them. After that they will magically disappear. So
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
global channel structure. Some basic rules can make sense (e.g. every
team should have a ``team-[name]`` channel as a way to contact them). 
Aside from that, trust people to self-organize into efficient groups 
and do the same for your own work. Don't fear being part of many, many,
channels! Use Slack's per-conversation notification settings and powerful
configuration options to ensure that you're part of the conversations that are
useful for you without impacting other peoples' options to communicate with
each other.

Message retention settings
~~~~~~~~~~~~~~~~~~~~~~~~~~
Message retention is an interesting topic. I generally like to set
message retention on "general chat" channels (e.g. #general) to around
30 days. I encourage you to think about the type of channel you have just
opened. If it's a general chat channel for your team, set a retention
policy. If it's a channel for a specific project however, retaining messages
is a good idea. Slack's archive should never be treated as a replacement 
for documentation or tickets. However, its archive is very useful, so 
thats's the balance you have to strike.

Naming a channel
~~~~~~~~~~~~~~~~
As a corollary of the above, I disagree with having intricate naming rules 
for Slack channels. However, I feel that it's worth doing just a little bit 
of due diligence before creating a channel:

1. Do a cursory check if a channel already exists that covers what you're 
   trying to do.
2. If there exists a channel for a similar thing you're doing, try to follow 
   that channel's naming pattern (e.g. if there are 6 channels called
   ``hiring-[jobname]`` don't create a seventh channel called 
   ``myjob_hire``). This groups related channels for people who are in
   every one.
3. Try to find a descriptive name for the channel's scope.
4. Remember that many channels will only be around for a couple of weeks, 
   don't worry about it too much.
5. If you come up with a better name later, just rename your channel.
6. If somebody points out another channel already serving your purpose,
   check if they're right and just move your conversations over there.


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
.. _HBR_Open_Offices: https://hbr.org/2019/11/the-truth-about-open-offices
.. _destalinator: https://github.com/randsleadershipslack/destalinator
.. _Nobody likes naked pings:
    https://blog.doismellburning.co.uk/nobody-likes-naked-pings/
