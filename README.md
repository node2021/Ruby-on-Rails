## Requirements
you are required to create and deploy a SaaS application using the Ruby on Rails framework, and write a comprenehsive suite of automated tests. You are free to come up with your own idea for what your application will do, but it can be broadly similar in style to the RottenPotatoes movie review sample application we worked on throughout the course (though obviously it must be different, i.e. not based on movies). In terms of functionality your application should be relatively simple. The focus here is not on building a complex feature-heavy application, but rather on building a simple application using solid engineering principles with thorough automated tests. Your application must conform to the specification detailed below.

### Specification 

#### Functionality
Your application should:
- support basic CRUD operations on a single resource (e.g. similar to the create, read, update and delete operations on movies supported by RottenPotatoes).
- support basic filtering and sorting functionality
- include at least one **additional feature** beyond the basic CRUD and filtering/sorting features we developed in labs. Possible options here include:
    - something like the RottenPotatoes "find movies by the same director" feature you worked on for Lab Assignment 5
 
#### Database
Your application should:
- use an SQL database in development and postgres in production (the relevant gems are included in the starter code). 
- define a database schema in a Rails migration, which can be used to create a database using the `rake db:migrate` task.
- define seed data which can be used to populate the database with initial data using the `rake db:seed` task.

#### Testing
Your application should include a comprehensive suite of automated tests, specifically:
##### Cucumber
- Cucumber BDD/Acceptance tests which verify the **additional feature** works as expected. Your cucumber tests should at a minimum include 2 scenarios, testing both the happy and sad paths of the feature. Comprehensive testing of the feature will be necessary to score full marks for this component.

##### RSpec
- RSpec unit/functional tests for the controller and model. Your RSpec tests should test:
  - the controller and model logic added to implement the **additional feature**.
  - whatever other controller/model logic that needs to be tested to improve code coverage.
 ##### Code Coverage
- The `simplecov` gem and necessary setup is included in the provided starter code. This will generate a detailed report of how well your code is covered by tests in `coverage/index.html`, as well as reporting the overall coverage percentage on the command line when `cucumber` and `rspec` tests are run (see CA5). Use this coverage report to identify under-tested code that you need to write tests for. Note that 100% coverage isn't necessary, or even desirable.
