Contributing to pimd
====================

pimd is a very old project.  As such it has a lot of history that
sometimes creep up through the cracks.  Bugs!

Bugs can be missing or unclear documentation, faulty legacy behavior,
missing key features or support for a new cool operating system.  Or
simple things, like speling errors or too frequent, or missing logs.

pimd exists on [GitHub][github] for this exact purpose -- to fix bugs,
collaboratively.

We welcome any and all help in the form of bug reports, fixes, patches
for new features -- *preferably as GitHub pull requests*, submitting a
pull request practically guarantees inclusion ... other methods are of
course also possible: emailing the maintainer a patch or even a raw
file, or simply emailing a feature request or an alert for a problem.
For email questions/requests/alerts there is always the risk of memory
exhaustion on the part of the maintainer.


Coding Style
------------

> **Tip:** Adapt your code to what the surrounding code looks like!

pimd is written in C.  C is an old language and sometimes that age is
clearly visible.  The current maintainer has tried to (re)enforce a
consistent and more modern C style, without having to completly
re-indent the whole code base.

First of all, lines are allowed to be longer than 72 characters these
days.  In fact, there exist no enforced maximum, but keeping it around
100 chars is good practice.

pimd use leading four spaces in functions and structs.  The next level
use eight spaces, but the original authors used tab for that level.  A
`switch()` has its `case` statements indented four spaces ... but then
it is more or less [KNF][].

In Emacs this coding style can be achieved by using the following
footer applied to a C file:

    /**
     * Local Variables:
     *  indent-tabs-mode: t
     *  c-file-style: "cc-mode"
     * End:
     */

The current maintainer has considered shifting the original coding
style to FULL [KNF][] several times, but decided against changing
to keep with the intent of the original authors.


Commit Messages
---------------

Commit messages exist to track *why* a change was made.  Try to be as
clear and concise as possible in your commit messages, and always, be
proud of your work and set up a proper GIT identity for your commits:

    git config --global user.name "Jane Doe"
    git config --global user.email jane.doe@example.com

Example commit message from the [Pro Git][gitbook] online book, notice
how `git commit -s` is used to automatically add a `Signed-off-by`:

    Brief, but clear and concise summary of changes
    
    More detailed explanatory text, if necessary.  Wrap it to about 72
    characters or so.  In some contexts, the first line is treated as
    the subject of an email and the rest of the text as the body.  The
    blank line separating the ummary from the body is critical (unless
    you omit the body entirely); tools like rebase can get confused if
    you run the two together.
    
    Further paragraphs come after blank lines.
    
     - Bullet points are okay, too
    
     - Typically a hyphen or asterisk is used for the bullet, preceded
       by a single space, with blank lines in between, but conventions
       vary here
    
    Signed-off-by: Jane Doe <jane.doe@example.com>


Target Systems
--------------

pimd mainly targets modern UNIX systems and has been tested on both
Debian and Ubuntu for Linux, FreeBSD, and NetBSD.  Please consider these
targets when submitting changes.  If you cannot test on them do this, be
prepared that your feature/fix will likely be delayed by the maintainer,
who will attempt to test and in some cases port the feature for you.


Code of Conduct
---------------

It is expected of everyone engaging in the project to, in the words of
Bill & Ted; [be excellent to each other][conduct].


[github]:   https://github.com/troglobit/pimd/
[KNF]:      https://en.wikipedia.org/wiki/Kernel_Normal_Form
[gitbook]:  https://git-scm.com/book/ch5-2.html
[conduct]:  CODE-OF-CONDUCT.md
