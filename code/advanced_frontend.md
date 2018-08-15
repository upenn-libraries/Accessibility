# Advanced Front-End Topics

So, you've got the [basics](guidelines.md) down. Your page hierarchy is in order, your links are spotless, validators are singing songs from the heavens, things are looking good. But now, you need to build custom navigation elements, forms, and Javascript-heavy features: what do you do?

It's relatively easy to build a custom page component, and there is the inclination to call it "done" and release it as soon as it looks like it works. But, no matter how much you love that shiny new tabbed interface you just made... do you know for certain that *everyone* can use it? If screen readers can't navigate your new menu, it's useless.

There are a couple of steps you can take toward making sure your custom work can be used by everyone visiting your page:

### 1.) Evaluate necessity.
Before embarking on custom work, it's important to consider: are we re-inventing the wheel? Are there pre-existing solutions available for what we need?
It's best to avoid custom components if you can, but when you can't, you need to set aside abundant time for testing and refining your component's accessibility.

### 2.) Test, test, and test again.
This one might seem obvious, but it's easy to neglect. Custom work requires careful testing to make sure..
* ..it is *navigable*.
* ..hidden/dynamic content is accessible by screen readers and keyboards.
* ..appropriate user control works without a mouse.
* ..it doesn't confuse/disorient the user, or otherwise interfere with normal browsing behavior.

### 3.) Look for accessibility *role*-models.
Check with W3C documentation for pre-existing examples of the behavior you're trying to achieve.
Unless you're doing some serious trailblazing, there are probably standards in place that you can follow to make your component accessible. For example, if you're trying to build a tabbed interface, W3C has numerous specifications on how to assign ARIA roles to those tabs.

Even if this component is really unique, you can probably break it down into a set of smaller components that *are* commonplace and have standards you can follow. Perhaps "Crazy Dave's Super-Duper Search Machine" is really just a set of tabs and HTML forms. Tomato, to-*mah*-to. Try to look beyond your group's internal wording and learn about the global verbiage that applies to your component, so that you can find documentation for it. This might require some serious Googling. Don't give up!

If you're really building something that nobody has ever thought of, you should set aside plenty of time to consider how people, especially disabled people, will navigate and use it. Skills and techniques used in UX design are helpful here.

### 4.) Write *mindful* Javascript.
If you're writing Javascript, make sure your DOM manipulations aren't so crazy that they destroy the navigability of your page. If you go nuts with your Javascript, validators probably aren't going to notice and you'll find out in a different way: either through testing, or through the words of angry user feedback, if you're fortunate enough to receive it.

Check out this site for basic JS accessibility issues to consider:
http://webaim.org/techniques/javascript/