# angular-9-testing-app
Application called shop4less for running tests in Angular with Angular 9 and Jasmine.js

## Up the project

- Clone this repo.

- Access the cloned repository and run in your terminal: 

        npm install && npm install json-server

- Up the backend on json-server with:

        npm run start-backend

- Open a new tab on your terminal and run this command below to up frontend:

        npm start

## Execute Unit Tests

    npm run test

## Execute E2E Tests

    npm run e2e
## Frameworks and Tooling used:


- Angular CLI 

- [Jasmine](#Jasmine-Framework)

- [Karma](#Karma-Framework)

- [Protractor](#Protractor-Framework)

- [Cucumber](#Cucumber-Framework)

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

## Protractor Framework

- Protractor is an open source E2E testing framework for Angular applications.

- It is built by a team in Google on the top of WebDriver.

- It also works as a solution integrator that combines powerful technologies such as
NodeJS, Selenium, Jasmine, WebDriver, Cucumber, Mocha etc.

- Along with testing of Angular application, we can also use Protractor for automated
regression tests for any web applications.

- It allows us to test our application just like a real user because it runs the test using an actual browser.

## Cucumber Framework

- Cucumber is a tool that supports Behaviour-Driven Development(BDD).

- Cucumber is Open Source software.

- Cucumber reads executable specifications written in plain text and validates that the
software does what those specifications say.

- The specifications consists of multiple examples, or scenarios.

- Gherkin is a set of grammar rules that makes plain text structured enough for
Cucumber to understand.


# Understanding Patterns and Specificities
## AAA Pattern
- Arrange - "arrange" everything like setup ground work for working with tests for execution.
- Act - Act on your unit test case, calling methods, processing data, etc.
- Assert - Verifying the actual data of test result and expected data.

### Example
    describe('AppComponent', () => {
        
        // Arrange

    beforeEach(async(() => {
        TestBed.configureTestingModule({
        imports: [
            RouterTestingModule
        ],
        declarations: [
            AppComponent
        ],
        }).compileComponents();
    }));

      it('should render title', () => {

          // Act

        const fixture = TestBed.createComponent(AppComponent);
        fixture.detectChanges();
        const compiled = fixture.nativeElement;

        // Assert

        expect(compiled.querySelector('.content span').textContent).toContain('shop4less app is running!');
        });
    });

## BeforeEach Method
- We use an async before each. The purpose of the async is to let all the possible asynchronous code to finish before continuing.


- Before running any test in angular you need to configure an angular testbed.


- This allows you to create an angular environment for the component being
tested.


- Any module, component or service that your tested component needs have to
be included in the testbed. Finally, after setting the configuration, you call the
compile components function.

## Angular TestBed (ATB)

- It creates an Angular testing module — a @Ng Module class — that you configure with the
configure Testing Module method to produce the module environment for the class you
want to test.


- Configures and initializes environment for unit testing and provides methods for creating
components and services in unit tests.


- It creates a dependency injection (DI) context and allows us to override providers, services,
and whole modules.


-  It compiles, instantiates, and renders to HTML our components attaching them to the fixture
instance. Any module, component or service that your tested component needs have to be
included in the testbed.


- Finally, after setting the configuration, you call the compile components function.

### Example

    beforeEach(() => {
        TestBed.configureTestingModule({})
        service1 = TestBed.inject(ProductService)
    })