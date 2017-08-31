# Front-end testing

Front-end testing is not integration, usability, or accessibility testing, but
rather focuses on the functional presentation of pages and elements to the
end user. As with any type of testing, there can be considerable overlap
between front-end testing and other testing types. Integration tests, for
example, can be written to test many front-end elements.

Front-end testing for web sites and applications should deal with:

- Presence of fields and features on pages

- Expected results based on inputs: Are user created and edited values
  reflected?

- CSS behavior and coverage

- JavaScript behavior across application pages

- Correct handling of user data

- Responsive page display

- Cross-browser display

### Feature and field presence

Front end testing should confirm that elements and data values appear or do
not appear on pages as expected. If an application has different levels of
access based on user roles, do users see the correct elements based on
roles: page sections, links, data values, etc?

Automated tools can readily test for the presence of items on a page. They may
also be used to test the relative order of elements on a page. For example,
you can use Ruby testing Gems Capybara and RSpec to test the relative order of
items on a web page:

<http://launchware.com/articles/acceptance-testing-asserting-sort-order>

Note though that automated testing has its limits. Building tests to check
field order can be time consuming and require considerable test-maintenance as
requirements change and mature. And, more importantly, a test of the relative
order of elements in the DOM will not reveal CSS effects that change the
display order elements or cause them to not be visible at all.

### Expected results based on input

Does user input show up as expected? Are user-created and user-modified
content displayed as expected?

### Error handling

- Bad input -- Does the interface alert users to bad input? -- numbers out
  of range, invalid email address, text values for numbers, and so on
- Correct display of error pages: 403, 404, 503, etc.

### CSS behavior and coverage

Does CSS display as expected and consistently across pages?

### JavaScript behavior

Does JavaScript behave consistently across all pages. Note that much
JavaScript behavior can be tested using automated tools. These are especially
good for testing complex behaviors as application code changes. Note though
that some tools that are used to test front-end behavior do not test
JavaScript. As always, automated testing is not a substitute for visually
confirming expected behavior.

### Responsive page display

Confirm that pages display correctly at all anticipated resolutions.

### Cross-browser display

Confirm that the application functions correctly across common browsers,
especially Chrome, Firefox, and Internet Explorer (Do people do this?).

