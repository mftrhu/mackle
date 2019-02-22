The making of -mackle
=====================
2017-12-08

**Why?** LaTeX is unwieldly, bloated and not installed by default on most
systems. Conversely, `groff` is almost everywhere, fast and very light
(verging on the skeletal) - but, except for when it's used with the `-mom`
macros, it suffers from a too terse and antiquated syntax.

These macros are an attempt to bridge the two worlds - make `groff` into
something *humans* can use, but without encumbering it overmuch.

They are the fruit of repeated attempts over the course of two months,
starting from the last days of October 2017 - the first iteration was
extremely limited in scope, aimed at the creation of simple (and somewhat
semantic, insofar semantic can be said of `groff` source) resumes.

The following iterations tried to iron out a couple of problems I found
with the `-mom` macros - namely, I didn't manage to find a way to have
multiple chapters within the same file, looking how I wanted them to
look. This, together with a first stab at `troff` preprocessors, thanks
to a Python script I found on GitHub to properly colorize and format code
snippets.

It worked, but it wasn't good enough.

By that point I stumbled across David Given's `-meta` macros, which were
very useful by demonstrating a few peculiarities of the language I was
still unacquainted with.

Like the fact I could dynamically define new variables, which is how he
implemented stacks in his macro package. Idea, promptly stolen.

This iteration went much better than the previous ones, providing me with
a great starting point, but I just. Couldn't. Get. The. Bloody. Footnotes.
To. Work.

`troff`'s diversions, intuitive they ain't.

I hammered them out, then they broke, then I hammered them out again, then
they broke, *repeat x1000*, then I realized I needed to rewrite the whole
thing because I wasn't accounting for footnotes that couldn't fit within
the current page.

Fourth iteration, abandoned for a week.

Enter the fifth iteration.

I decided to put every facet of my macro package in its own file, with
a primitive version of namespaces to avoid any issues.

I slowly worked my way through the primitives - some aliases to make my
life easier, the stack/array macros from before, macros to handle fonts,
to set the page size, the margins, and style.

Then, finally, came the footnotes.

The whole thing got re-written from scratch, accounting for overflow,
with proper sizing, with my hard-gotten knowledge of diversions and study
of the `-ms` and `-mm` packages.

And.

It.

Worked.

Not flawlessly, not at first, but I chipped at it, tweaked things here
and there, liberally sprinkled the whole things with `.tm` macros, and
now they do - while being relatively configurable to boot!
