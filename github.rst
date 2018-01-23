Baseline principles of using GitHub
===================================

There are a million ways to use GitHub. As a CTO I have strong opinions on how
GitHub should be used. Some aspects require a tailored approach for each
individual organization. I do feel however, that I'm able to extract some
baseline rules for interacting with GitHub that improve everybodys' lifes.

I want to start with an ABC of the things that *do* require careful individual
consideration though.

Things you need to consider specifically for your organization
--------------------------------------------------------------

"A" is for access
~~~~~~~~~~~~~~~~~
You need to be clear who needs access to what. This is a hard job. Especially,
if your organization is small (less than 50 developers), there is little point
in separating information too much. An argument can be made that all developers
should have at least read-only access to all repositories, even in large
organizations, or at least within the product they're working on.

Most security arguments about code sharing are bogus. But inefficiencies through
lacking knowledge sharing or access to knowledge are very real.

As I will repeat below, you should protect your ``master`` branch, so that
developers can't just commit to it whenever. Code review makes sense, almost
always. At the very least, once you've hit "1.0", your master branch should
be protected. For security-relevant code it makes sense to allow only a certain
group of people to review the code.

If you're working on software containing information that must be protected
(licensed code, trade secrets, etc.), create an actual threat model and attacker
model and *write it down*. Then create access rules that allow for good
collaboration and a high grade of process support (see below). Don't just
blindly limit access adhoc.

"B" is for branching
~~~~~~~~~~~~~~~~~~~~
You have to take a long, hard look at your branching model and how it relates to
your versioning model and how versions are used across parts of your code that
depend on them. This is **hard**. Don't just "do whatever", ensure that your
versioning model interacts well with how your product managers develop features
from stakeholder demand and how you release software. Finally, make sure that
you understand how your software manages artifact versions and how these
interact with deploying a specific commit (e.g. for integration environments and
local development), a specific tag or branch (for testing) and a specific
version of your software (for qa, releases and bug analysis). A mismatch between
these processes will create tremendous pain.

Don't blindly adopt "some strategy". But make sure you know `Git Flow`_,
`Github Flow`_ and `Semantic Versioning`_ and that you understand their pros
and cons.

Have a clear way for how development tasks (commonly user stories, tasks,
bugs and the like) make it into code. Then make sure that all development
follows that process and that the software you're using to connect to your
code delivers the maximum *process support grade* possible. That means:
your buildserver, wiki, ticket tracker, thingamajicky... use them to the
fullest extent possible to support your development processes, product
management processes and release processes. A mismatch between these will
create tremendous pain.

"C" is for committing
~~~~~~~~~~~~~~~~~~~~~
At the very least, at the end of the day, commit all code to a repo. If it's
unfinished, commit it to a branch. Never leave code uncommitted.

You might be tempted to sometimes not commit code you've written, because it
"isn't finished", "it's not ready". You're wrong. There are multiple things at
play here. One of them is: you might get hit by a bus. And even if that doesn't
happen, it's not the kind of culture that I as a CTO want in my organization and
I wouldn't recommend for yours. If you don't feel comfortable sharing unfinished
work or results that might betray that you're not an expert at something, There
is a larger problem with your culture that needs to be addressed.

So, at the end of the day: always commit your code. And just like with `Slack
communication`_: **fail open!** Share your code, share your mistakes, learn
from your peers.


Without further ado: Good practice for GitHub and Git repositories
------------------------------------------------------------------
In my opinion, the following things are good hygiene.

Every repository must have a description and a README
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
These are just not up for discussion :). Every repository must have a README
that contains at a minimum the following information or links to it:

* What software does this repo contain
* How to use it (e.g. compiling instructions, installation instructions,
  configuration reference)
* If it's anything but an internal project: The applicable license.

Commit a .gitignore to every project
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
You might have a default `.gitignore` in your organization, tailored to tools
you regularly use. You might also have a global `.gitignore` in your git config.
There seem to be two schools of thought on this. I believe firmly that every
Git repository should have a `.gitignore` that contains everything ever
discovered while working on that repository that should be ignored by Git. I
have yet to be part of a project where someone wanted to specifically track a
type of file that someone else wanted to ignore. And even then, you just have
to specifically `git add` that file once.

Ratchet your test coverage
~~~~~~~~~~~~~~~~~~~~~~~~~~
"Ratcheting" means to use one of the many services or tools that read
``coverage`` information (for example `coveralls <https://coveralls.io/>`__)
and failing the build when the test coverage goes down. As a good friend and
my previous co-CTO once said (I'm paraphrasing here from memory):
"100% test coverage tells you _something_. 0% test coverage also tells you
_something_. 80% test coverage tells you nothing, because you don't know
whether you've missed important parts."

There is no reason not to improve over the status quo.

Never skip code review
~~~~~~~~~~~~~~~~~~~~~~
If you have access to another developer, always let them review your code. It
improves cross-domain knowledge, catches bugs and edge cases, trains people on
each other's code and facilitates knowledge sharing. Once your project hits a
milestone like "version 1.0", it's also a good idea to protect your main
branches (like commonly ``master`` and/or ``develop``) to ensure that no
unreviewed code makes it into the repository. Use GitHub's tools to enforce
this.

If possible, introduce mandatory commit signing
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Git is really bad at tracking identity. A repository that does not let
unsigned commits enter the main line creates a direct line of trust for each
developer to every line of code they wrote. It's a great tool for security-
concious companies. It's also really hard to fix a repository that has any
unsigned commits (resigning commits creates new commit ids), so make that
decision early.

Integrate with CI as early as possible
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
With the availability of great tools like `CircleCI <https://circleci.com/>`_,
`TravisCI <https://travisci.org/>`_ and `Concourse.CI <https://concourse.ci/>`_
and even good old Jenkins, there is no excuse to not run your tests on every
single commit. Even before you have written any tests, running a Linter,
perhaps a static analyzer like `mypy <https://mypy-lang.org/>`_ for Python,
or even just your language's compiler, is a great tool to get a simple baseline
for code quality going.

Ensure baseline configuration across all repositories
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Use the `Terraform Github Provider`_ or write your own GitHub API client, but
if your organization has more than 10 repositories, definitely regularly run a
script that ensures common baseline configuration. For example: All repositories
should have a webhook that connects them to your ticket tracker or calls your
IRC/Slack Bot. All developers should have access to all repositories (unless
your orgnaization is really big, as discussed above). You want to ensure that
your repository names match a certain template and set the master branch to
be protected. Things like that.


.. _Git Flow: http://nvie.com/posts/a-successful-git-branching-model/
.. _GitHub Flow:
   https://guides.github.com/introduction/flow/?utm_source=onboarding-
   series&utm_medium=email&utm_content=read-the-guide-cta&utm_campaign=
   learn-github-flow-email
.. _Semantic Versioning: https://semver.org/
.. _Slack communication:
   https://github.com/jdelic/reimagined-spoon/blob/master/slack.rst
.. _Terraform GitHub Provider:
   https://www.terraform.io/docs/providers/github/index.html
