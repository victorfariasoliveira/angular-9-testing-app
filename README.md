# angular-9-testing-app
Application called shop4less for running tests in Angular with Angular 9 and Jasmine.js

## Frameworks and Tooling used:
- Angular CLI
- Jasmine
- Karma
- Protractor
- Cucumber

## Understanding Testing Concepts in Angular 
- Unit Testing
    - Testing smaller granular independent modules, services, pipes is called as unit testing.
    - Focus in on "task" level testing.
    - Provides input and verifies output for smaller samples.
    - Ideal for testing individual pieces of the big picture.
    - Frameworks used are Jasmine and Karma. 
        - Jasmine is the framework to writing yours tests and Karma is the runner.

- End to End Testing
    - Automating the end to end functional flows.
    - Helps in building automated test suites when application or product sizes outgrowns.
    - Ṕrotractor framework is used for End to End Testing.
    - BDD frameworks like Cucumber are also used for testing the functional flows.

## Testing Utilities Provided by Angular

- Auto generation of code.
- Angular natively supports unit tests using Jasmine and Karma.
- Angular CLI has build-in commands to run unit tests.
- Angular CLI has build-in commands to run End to End tests.
- Using Angular CLI - We generate the test files (spec).
- We can also use Angular In-Memory service to mock the services of application.
- Angular provides easy way to Mock Services and use Class which will helps in testing.
- Support for extending and using othe frameworks BDD (Cucumber).

## Jasmine Framework

- Jasmine is a open source testing framework for javascript.
- Jasmine is BDD (Behavior Drive Development) testing framework.
- In BDD - the test are written in non-technical language which makes it easy for Business Analysts too to write test specs.
- It does not require any javascript framework.
- Also Jasmine has native support for Async testing.
- Jasmine supports Spy objects using which we can target an element we want to test.
### Basic Syntax End to End Testing Example
    describe('appComponent', () => {
        It('it should navigate', () => {
            console.log('navigated to page')
        })
    })

## Karma Framework
- Karma is an open source testing framework for JavaScript.
- Karma is created and maintained primarily by the core Angular team.
- The framework is natively integrated into the Angular apps by default.
- Since it's integrated, we can easily run our tests from the CLI console.
- One of the striking features is the ability to run on different browsers resolutions like Tablet, Mobile...
- Karma is used for running and executing the test scripts.
- Hence the framework plays well with other JavaScript frameworks like Jasmine, Mocha...
- The frameworķ can be integrated right into the build pipelines which means it will run in
our build and deployment pipelines.
    - Automating the entire end to end functional flows.
    - Helps in building automated test suites when the application or product sizes outgrows.
    - Protractor framework is used for End to End Testing.
    - BDD frameworks like Cucumber are also used for testing the functional flows.