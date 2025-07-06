# Azure DevOps Test Plans
Test Plans in Azure DevOps are a full-featured testing suite for:
- Manual Testing
- Exploratory testing
- Automated testing integration
- Test result tracking & reporting

## Test Plans Core Components:
1. **Test PLan** <br>
A Test Plan is a container for test cases that target a particular release, sprint, or feature set. <br>
it contains test suites and test cases. You can create multiple test plans per project <br>

2. **Test Suites**  <br>
Inside a test plan, you can organize tests into suites:
- Static                  -> Manually group test cases
- Requirement-based	      -> Automatically create test cases for linked work items (e.g. User Stories)
- Query-based	            -> Include test cases dynamically based on a query

3. **Test Cases**  <br>
Each test case defines:
- A set of steps to execute
- Expected results
- Associated work items

4. **Test Runs**  <br>
A test run is an execution of test cases, either:
- Manual (step-by-step execution)
- Automated (via pipeline)
- Exploratory (freeform testing session)

Each run records:
- Status (pass/fail/blocked)
- Bug reporting
- Screenshots, attachments
- Tester identity and time

## Integration with Azure Boards
- Each test case can be linked to user stories, bugs, features
- Requirement-based suites can auto-generate test cases from work items

## Integration with Pipelines (Automated Testing)
You can run automated tests from Pipelines and publish results to Test Plans. <br>
Results show up in Test Runs with full history.
