# Testing Techniques &amp; Tools

## Unit Testing

Unit testing consists of tests that cover small pieces (units) of code, typically individual functions or modules.

## Integration Testing

Integration testing is larger in scope than unit testing and consists of tests that cover multiple units of code and their behavior when working together.

## Code Coverage

Code coverage is a measure of the lines of code executed by unit and integration tests. Code coverage should not necessarily be used as a code quality measure. Instead, it should be treated as a tool by test authors to verify that the test suite does miss any large chunk of code.

## Testing Libraries

Testing libraries assist with writing and executing tests and are often technology-specific (see [RSpec](http://rspec.info/), [JUnit](http://junit.org/), [PHPUnit](https://phpunit.de/)).

## Stubs

Stubs are pieces of code that are used in place of dependencies for the code being tested to simplify testing. For example, a stub can be used to return canned search results or simulate a user logging in rather than having to have a working integration with the respective external systems.
