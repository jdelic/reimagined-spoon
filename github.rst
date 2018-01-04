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
developers can just commit to it whenever. Code review makes sense, almost
always. At the very least, once you've hit "1.0", your master branch should
be protected.

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

"C" is for communication
~~~~~~~~~~~~~~~~~~~~~~~~
Have a clear way for how development tasks (commonly user stories, tasks,
bugs and the like) make it into code. Then make sure that all development
follows that process and that the software you're using to connect to your
code delivers the maximum *process support grade* possible. That means:
your buildserver, wiki, ticket tracker, thingamajicky... use them to the
fullest extent possible to support your development processes, product
management processes and release processes. A mismatch between these will
create tremendous pain.

Without further ado: Good practice for GitHub and Git repositories
------------------------------------------------------------------
In my opinion, the following things are good hygiene.

Every repository must have a description and a README
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

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

Integrate with CI as early as possible
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ratchet your test coverage
~~~~~~~~~~~~~~~~~~~~~~~~~~

Ensure baseline webhook configuration across all repositories
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~






.. _Git Flow: http://nvie.com/posts/a-successful-git-branching-model/
.. _GitHub Flow:
   https://guides.github.com/introduction/flow/?utm_source=onboarding-
   series&utm_medium=email&utm_content=read-the-guide-cta&utm_campaign=
   learn-github-flow-email
.. _Semantic Versioning: https://semver.org/
