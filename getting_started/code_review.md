# Code review & Continuous Integration

If your development team has a workflow for testing code, you can find ways to introduce accessibility into the process that's already working well for you. It's desirable to find a simple way to encourage ownership and shared responsibility for accessibility in all stages of development, *especially* in testing!

## Code reviews
* If your team already performs regular code reviews, there is no reason not to include accessibility in those reviews.
* In order to simplify the process, you could establish a short checklist of "low-hanging fruit" ([level 1 tasks]({{site.baseurl}}/getting_started/guidelines)) to always test for in your daily code reviews, and give a pass/fail based on those standards.
  * You could also establish recurrent weekly/monthly tests for more difficult tasks or complicated projects.

## Continuous Integration (CI)
* CI involves automatically building and testing code, with the end goal of developers integrating their code into their master repository several times a day. It's a methodology of "build quickly, test often", intended to increase frequency of releasing new features, and detect bugs as soon as they are written and before they get set in stone.
* Accessibility does not have to be antithetical to CI, but it might require creative solutions to achieve harmony.
* You probably won't want to include automated accessibility validators/tests in your CI test suite. Very often, a11y testers throw false-positives, and you don't want that to get in the way of submitting your code. But you can come up with alternatives:
  * Instead of automated testing, you could add in a step for an accessibility code review as described earlier.
  * You could create a small-scale test suite that checks for low-hanging fruit. Add the ability to ignore/dismiss false-positives, if needed.
