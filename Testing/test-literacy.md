
# Testing Literacy

## What We Talk About When We Talk About Testing

Testing means verifying that software works as specified. It sounds
simple, but testing is one of the hardest disciplines in software
engineering to do well.

## Guidelines

- Don't assume. Casual testers sometimes fall into a trap of circular
  reasoning: if the software does something, it must be right, and a
  behavior must be right because that's how the software works. Before
  you start testing, have a set of clear specifications and
  expectations; the job of the tester is to make sure the system
  really lives up to them.

- Describe problems you find as precisely as you can. Examples of
  unhelpful bug descriptions:

  "The login link is broken."
  "Search doesn't work."

  Helpful bug descriptions often include the expected behavior
  ("should" is a good word to use):

  "The login link takes me to a mostly blank white page that says 'Not Found'"
  "Searching for Robinson Crusoe returns 0 results but there are definitely 3 books that should show up"

- Include a list of steps to reproduce the bug. What did you do to
  trigger the error message or the unexpected behavior? If there's
  more than one way to do what you're trying to do, are they all
  broken or is just one of those methods broken? Does it happen all
  the time or only sometimes? Does the problem seem to only happen
  under certain circumstances or in certain environments (e.g. only on
  your home computer, or only in Firefox but not in Chrome)? Did it
  used to work at some point in time, or to your knowledge was it
  always broken?

- Regressions. Changes made to software can often affect it in broad
  ways or have an impact on related subsystems. For example, if a
  developer fixes a bug on the advanced search page of discovery, it
  could potentially affect the behavior of other searches. When a
  change inadvertantly breaks something that used to work, it's called
  a regression.

  When testing new features added to software or updates, talk to
  developers to get a sense of what related things might be good to
  test, beyond the specific functionality in question. This will help
  catch regressions.

- Software is always growing and changing over multiple iterations of
  the
  [software development lifecycle](https://www.tutorialspoint.com/software_engineering/software_development_life_cycle.htm).
  Testing is a crucial part of that process, not something extraneous to it.
