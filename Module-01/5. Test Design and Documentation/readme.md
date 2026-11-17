# Test Design, Execution and Closure

## Table of Contents

1. Test Design Techniques
2. Use Cases
3. Test Scenarios
4. Test Cases
5. Test Environment and Execution
6. Defect Reporting
7. Test Closure
8. Difference Between Important Testing Terms
9. Practical Example: E-commerce Application
10. Interview Questions and Answers
11. Practical Assignments
12. Chapter Summary

---

# 1. Test Design Techniques

## What Are Test Design Techniques?

Test Design Techniques are methods used by software testers to identify and create effective test cases.

They help testers decide:
- What should be tested?
- Which inputs should be provided?
- What conditions should be checked?
- How can we find maximum defects with minimum test cases?

Instead of testing randomly, testers use systematic techniques to design meaningful test cases.

### Why Are Test Design Techniques Important?

1. Improve test coverage.
2. Help identify defects early.
3. Reduce unnecessary test cases.
4. Save testing time and effort.
5. Improve overall software quality.
6. Ensure important conditions are not missed.

## Types of Test Design Techniques

Test design techniques are commonly divided into three categories:

1. Black Box Testing Techniques
2. White Box Testing Techniques
3. Experience-Based Testing Techniques

### 1.1 Black Box Testing Techniques

Black Box Testing techniques focus on application inputs and outputs without considering the internal code structure.

Important techniques include:

#### A. Equivalence Partitioning

Equivalence Partitioning divides input data into groups called equivalence classes.

The assumption is that values within the same group should behave similarly. Therefore, instead of testing every value, we select representative values from each group.

**Example:**

Suppose an application accepts an age between 18 and 60.

| Input Group | Values | Expected Result |
|---|---|---|
| Below minimum | Less than 18 | Invalid |
| Valid range | 18–60 | Accepted |
| Above maximum | Greater than 60 | Invalid |

Instead of testing every possible age, we can select:
- 15 – Invalid
- 30 – Valid
- 65 – Invalid

**Advantages:**
- Reduces the number of test cases.
- Saves testing time.
- Provides systematic input coverage.

#### B. Boundary Value Analysis (BVA)

Boundary Value Analysis focuses on testing values at the boundaries of input ranges.

Defects frequently occur around minimum and maximum limits.

**Example:**

Suppose the valid age range is 18 to 60.

| Test Input | Expected Result |
|---|---|
| 17 | Invalid |
| 18 | Valid |
| 19 | Valid |
| 59 | Valid |
| 60 | Valid |
| 61 | Invalid |

The important boundary values are:
- Minimum boundary: 18
- Maximum boundary: 60

We also test values immediately below and above these boundaries.

**Advantages:**
- Helps identify boundary-related defects.
- Useful for fields with minimum and maximum limits.
- Provides effective test coverage with fewer test cases.

#### C. Decision Table Testing

Decision Table Testing is used when application behavior depends on multiple conditions.

A decision table represents different combinations of conditions and their expected actions.

**Example: Login Application**

Conditions:
- Correct username?
- Correct password?

| Rule | Username | Password | Expected Result |
|---|---|---|---|
| 1 | Correct | Correct | Login Successful |
| 2 | Correct | Incorrect | Login Failed |
| 3 | Incorrect | Correct | Login Failed |
| 4 | Incorrect | Incorrect | Login Failed |

**Advantages:**
- Covers combinations of conditions.
- Useful for business rules.
- Helps identify missing requirements.

#### D. State Transition Testing

State Transition Testing checks how an application behaves when it moves from one state to another.

It is useful when application behavior depends on previous actions.

**Example: ATM PIN Verification**

An ATM allows a maximum of three incorrect PIN attempts.

| Current State | User Action | Next State |
|---|---|---|
| Active | Correct PIN | Access Granted |
| Active | Incorrect PIN | One Attempt Used |
| One Attempt Used | Incorrect PIN | Two Attempts Used |
| Two Attempts Used | Incorrect PIN | Card Blocked |

**Advantages:**
- Useful for applications with multiple states.
- Identifies incorrect state changes.
- Tests behavior after repeated actions.

#### E. Use Case Testing

Use Case Testing derives test cases from user interactions with an application.

It focuses on validating complete user workflows.

**Example: Online Shopping**

1. User opens the application.
2. User logs in.
3. User searches for a product.
4. User adds the product to the cart.
5. User proceeds to checkout.
6. User completes payment.
7. Order confirmation is displayed.

The tester verifies whether the complete workflow works correctly.

### 1.2 White Box Testing Techniques

White Box Testing techniques focus on the internal code structure and logic of an application.

These techniques generally require programming knowledge.

#### A. Statement Coverage

Statement Coverage checks whether every executable statement in the source code has been executed at least once.

**Example:**

```javascript
function checkAge(age) {
    if (age >= 18) {
        console.log("Eligible");
    }

    console.log("Check completed");
}
```

Calling `checkAge(20)` executes both statements.

Calling `checkAge(15)` executes only the second statement.

#### B. Branch Coverage

Branch Coverage checks whether each possible outcome of a decision has been executed.

For example, an `if-else` statement has two branches:
- True branch
- False branch

Both branches should be tested.

#### C. Path Coverage

Path Coverage checks different possible execution paths through the program.

It is generally more comprehensive than statement or branch coverage, but complete path coverage can become impractical when many combinations exist.

### 1.3 Experience-Based Testing Techniques

These techniques use the tester's knowledge, experience, intuition, and understanding of the application.

#### A. Error Guessing

Error Guessing is a technique in which testers predict possible defects based on previous experience.

**Example: Login Page**

A tester may check:
- Empty username.
- Empty password.
- Special characters.
- Very long input.
- Incorrect credentials.
- Spaces before or after input.
- Repeated login attempts.

#### B. Exploratory Testing

Exploratory Testing involves learning the application, designing tests, and executing them simultaneously.

The tester explores the application to discover unexpected problems.

#### C. Checklist-Based Testing

Checklist-Based Testing uses a predefined list of points that testers must verify.

**Example: Login Page Checklist**

- [ ] Username field is visible.
- [ ] Password field is visible.
- [ ] Login button works.
- [ ] Empty credentials are handled.
- [ ] Invalid credentials display an error.
- [ ] Password is masked.
- [ ] Forgot Password link works.

### Difference Between Test Design Techniques

| Technique | Main Purpose |
|---|---|
| Equivalence Partitioning | Divide inputs into groups |
| Boundary Value Analysis | Test boundary values |
| Decision Table Testing | Test combinations of conditions |
| State Transition Testing | Test state changes |
| Use Case Testing | Test complete user workflows |
| Statement Coverage | Execute code statements |
| Branch Coverage | Execute decision outcomes |
| Path Coverage | Test execution paths |
| Error Guessing | Predict defects using experience |
| Checklist-Based Testing | Verify predefined points |

---

# 2. Use Cases

## What Is a Use Case?

A Use Case describes how a user interacts with a system to achieve a particular goal.

It explains the interaction between an actor and the application.

An actor can be:
- A customer.
- An administrator.
- An employee.
- Another external system.

**Example:**

In an online shopping application, a customer uses the application to purchase a product.

### Main Components of a Use Case

1. Use Case Name
2. Actor
3. Preconditions
4. Main Flow
5. Alternative Flow
6. Exception Flow
7. Postconditions

### Example: Login Use Case

**Use Case Name:** User Login

**Actor:** Registered User

**Preconditions:**
- User must have an account.
- Application must be accessible.

**Main Flow:**
1. User opens the login page.
2. User enters a valid username.
3. User enters a valid password.
4. User clicks the Login button.
5. System validates the credentials.
6. System redirects the user to the dashboard.

**Alternative Flow:**
- User clicks Forgot Password.
- System redirects the user to the password recovery page.

**Exception Flow:**
- User enters an incorrect password.
- System displays an error message.

**Postcondition:**
- User successfully logs in or remains on the login page.

### Why Are Use Cases Important?

- Help understand user requirements.
- Identify complete business workflows.
- Help testers create test scenarios.
- Improve communication between developers, testers, and business analysts.
- Help identify missing functionality.

---

# 3. Test Scenarios

## What Is a Test Scenario?

A Test Scenario is a high-level description of what needs to be tested.

It represents a particular functionality or situation that should be verified.

In simple words:

**A Test Scenario tells us WHAT to test.**

### Example: Login Page

Possible test scenarios:

1. Verify login with valid credentials.
2. Verify login with invalid credentials.
3. Verify login with empty username.
4. Verify login with empty password.
5. Verify login with both fields empty.
6. Verify password masking.
7. Verify Forgot Password functionality.
8. Verify account lockout after repeated failed attempts, if required.
9. Verify login using special characters.
10. Verify login using keyboard navigation.

### Characteristics of Good Test Scenarios

- Clear and understandable.
- Based on requirements.
- Cover important functionality.
- Include positive and negative conditions.
- Avoid unnecessary duplication.
- Traceable to requirements.

### Types of Test Scenarios

**Positive Test Scenario:** Checks whether the application works with valid input.

Example: Login using a correct username and password.

**Negative Test Scenario:** Checks whether the application handles invalid input correctly.

Example: Login using an incorrect password.

**Boundary Test Scenario:** Checks behavior at input limits.

Example: Entering a password at its minimum and maximum allowed lengths.

### Test Scenario vs Test Case

| Test Scenario | Test Case |
|---|---|
| High-level description | Detailed testing instructions |
| Explains what to test | Explains how to test |
| Usually contains fewer details | Contains steps, data, and expected results |
| Can have multiple test cases | Covers a specific condition or flow |

---

# 4. Test Cases

## What Is a Test Case?

A Test Case is a documented set of instructions, inputs, preconditions, and expected results used to verify a particular application functionality.

In simple words:

**A Test Case tells us HOW to test something.**

### Components of a Test Case

A standard test case may contain:

| Field | Description |
|---|---|
| Test Case ID | Unique identification number |
| Test Scenario | Functionality being tested |
| Test Case Title | Short description |
| Preconditions | Conditions required before execution |
| Test Steps | Actions performed by the tester |
| Test Data | Input values used |
| Expected Result | Correct expected behavior |
| Actual Result | Actual application behavior |
| Status | Pass, Fail, Blocked, etc. |
| Priority | Importance of the test case |
| Severity | Impact of a defect, if one is found |
| Remarks | Additional information |

### Example: Login Test Cases

**Test Case ID:** TC_LOGIN_001

**Title:** Verify login with valid credentials.

**Preconditions:**
- User must have a registered account.
- Login page must be accessible.

**Test Data:**
- Username: testuser@gmail.com
- Password: ValidPassword123

**Test Steps:**
1. Open the application.
2. Navigate to the login page.
3. Enter a valid username.
4. Enter a valid password.
5. Click the Login button.

**Expected Result:**
- User should successfully log in.
- User should be redirected to the dashboard.

**Actual Result:**
- To be filled during execution.

**Status:** Not Executed

### Additional Test Cases

| Test Case ID | Test Description | Expected Result |
|---|---|---|
| TC_LOGIN_001 | Login with valid credentials | Login successful |
| TC_LOGIN_002 | Login with invalid password | Error message displayed |
| TC_LOGIN_003 | Login with invalid username | Error message displayed |
| TC_LOGIN_004 | Login with empty username | Validation message displayed |
| TC_LOGIN_005 | Login with empty password | Validation message displayed |
| TC_LOGIN_006 | Login with both fields empty | Required-field messages displayed |
| TC_LOGIN_007 | Check password masking | Password should be hidden |
| TC_LOGIN_008 | Click Forgot Password | Password recovery page opens |

### Types of Test Cases

**1. Positive Test Cases**

Verify that the application works with valid inputs.

Example: Entering correct login credentials.

**2. Negative Test Cases**

Verify that the application handles invalid inputs.

Example: Entering an incorrect password.

**3. Functional Test Cases**

Verify that a feature works according to requirements.

Example: Verify that the Add to Cart button adds the selected product.

**4. UI Test Cases**

Verify the appearance and behavior of user interface elements.

Example: Verify button alignment and field labels.

**5. Boundary Test Cases**

Verify minimum and maximum input values.

Example: Test an age field that accepts values from 18 to 60.

### Characteristics of a Good Test Case

A good test case should be:

- Clear.
- Simple.
- Specific.
- Reusable where appropriate.
- Traceable to requirements.
- Independent where practical.
- Easy to execute.
- Associated with an expected result.

### Test Case Writing Best Practices

1. Use unique test case IDs.
2. Write clear test steps.
3. Include realistic test data.
4. Define measurable expected results.
5. Cover positive and negative conditions.
6. Avoid combining unrelated tests.
7. Keep test cases updated when requirements change.

---

# 5. Test Environment and Execution

## What Is a Test Environment?

A Test Environment is the setup in which software testing is performed.

It includes the required hardware, software, network, database, tools, and configurations.

### Components of a Test Environment

1. Hardware
2. Operating System
3. Browser
4. Application Build
5. Database
6. Network
7. Testing Tools
8. Test Data
9. Server Configuration

### Example

Suppose we are testing an e-commerce website.

Our test environment may include:

| Component | Example |
|---|---|
| Operating System | Windows 11 |
| Browser | Google Chrome |
| Application | E-commerce website |
| Database | MySQL |
| Server | Development server |
| Network | Internet connection |
| Test Data | Registered customer accounts |

### Types of Test Environments

**1. Development Environment**

Used by developers to build and test application features during development.

**2. Testing/QA Environment**

Used by testers to execute test cases and identify defects.

**3. Staging Environment**

A production-like environment used for final verification before release.

**4. Production Environment**

The live environment used by actual customers.

### What Is Test Execution?

Test Execution is the process of running test cases against the application and comparing actual results with expected results.

### Steps in Test Execution

1. Understand the requirements.
2. Prepare test cases.
3. Set up the test environment.
4. Prepare test data.
5. Execute test cases.
6. Compare actual and expected results.
7. Record test results.
8. Report defects.
9. Retest fixed defects.
10. Perform regression testing when required.

### Test Execution Status

| Status | Meaning |
|---|---|
| Pass | Actual result matches expected result |
| Fail | Actual result does not match expected result |
| Blocked | Test cannot be executed due to a dependency or issue |
| Not Executed | Test has not yet been executed |
| Not Applicable | Test does not apply to the current scope |

### Example

**Test Case:** Verify login with valid credentials.

**Expected Result:** User should reach the dashboard.

**Actual Result:** User reaches the dashboard.

**Status:** PASS

Another example:

**Test Case:** Verify login with an incorrect password.

**Expected Result:** An appropriate error message should appear.

**Actual Result:** Application crashes.

**Status:** FAIL

A defect should be reported for the second case.

---

# 6. Defect Reporting

## What Is a Defect?

A Defect is a flaw or problem in software that causes the application to behave differently from the expected behavior or specified requirements.

It is also commonly called a bug.

### What Is Defect Reporting?

Defect Reporting is the process of documenting and communicating a defect found during testing to the development team.

A defect report provides enough information for developers to understand, reproduce, investigate, and fix the issue.

### Components of a Defect Report

| Field | Description |
|---|---|
| Defect ID | Unique defect identification |
| Defect Title | Short description of the issue |
| Description | Detailed explanation |
| Steps to Reproduce | Steps to recreate the defect |
| Expected Result | What should happen |
| Actual Result | What actually happened |
| Severity | Impact of the defect |
| Priority | Urgency of fixing the defect |
| Environment | Environment where defect occurred |
| Attachments | Screenshots, videos, logs |
| Reported By | Person who reported the defect |
| Status | Current defect status |

### Example of a Defect Report

**Defect ID:** BUG_LOGIN_001

**Title:** Application crashes when user enters an incorrect password.

**Description:**

When a user enters a registered email address with an incorrect password and clicks the Login button, the application crashes instead of displaying an appropriate error message.

**Steps to Reproduce:**

1. Open the application.
2. Navigate to the login page.
3. Enter a registered email address.
4. Enter an incorrect password.
5. Click the Login button.

**Expected Result:**

The application should display an appropriate error message, such as "Invalid username or password."

**Actual Result:**

The application crashes.

**Severity:** Critical

**Priority:** High

**Environment:**
- OS: Windows 11
- Browser: Google Chrome
- Environment: QA

**Attachment:** Screenshot or screen recording.

### Defect Life Cycle

The Defect Life Cycle describes the different stages a defect goes through from identification to closure.

Common defect statuses include:

1. New
2. Assigned
3. Open
4. Fixed
5. Retest
6. Verified
7. Closed
8. Reopened
9. Rejected
10. Duplicate
11. Deferred
12. Not a Bug

### Defect Life Cycle Explanation

**1. New**

Tester identifies and reports a new defect.

**2. Assigned**

The defect is assigned to a developer or responsible team member.

**3. Open**

The developer investigates the defect.

**4. Fixed**

The developer makes changes to resolve the defect.

**5. Retest**

The tester tests the fixed functionality again.

**6. Verified**

The tester confirms that the reported issue has been resolved.

**7. Closed**

The defect is closed after successful verification.

**8. Reopened**

If the issue still exists after the fix, the tester reopens the defect.

### Other Possible Defect Statuses

- **Rejected:** The reported issue is not accepted as a valid defect.
- **Duplicate:** The same defect has already been reported.
- **Deferred:** The defect will be addressed in a future release.
- **Not a Bug:** The behavior is expected according to requirements.

The exact defect workflow may differ between organizations and project tools.

### Severity vs Priority

These two terms are important in software testing interviews.

**Severity:** Severity describes how seriously a defect affects the application.

**Priority:** Priority describes how urgently the defect should be fixed.

#### Severity Levels

| Severity | Meaning | Example |
|---|---|---|
| Critical | Application or major functionality is unusable | Application crashes on startup |
| High | Major functionality is affected | Users cannot complete payments |
| Medium | Functionality is partially affected | Search filter gives incorrect results |
| Low | Minor issue | Small text alignment problem |

#### Priority Levels

| Priority | Meaning |
|---|---|
| High | Fix immediately or as soon as possible |
| Medium | Fix in the planned development cycle |
| Low | Can be fixed later |

### Difference Between Severity and Priority

| Severity | Priority |
|---|---|
| Measures impact | Measures urgency |
| Usually assessed by QA and technical teams | Often decided with input from business and project stakeholders |
| Focuses on how badly the application is affected | Focuses on when the defect should be fixed |
| Example: Payment failure | Example: Urgent fix before a major release |

**Interview Example:**

A spelling mistake on the homepage may have:
- Low Severity
- High Priority

Why?

Because the technical impact is small, but the homepage is highly visible and important to the business.

---

# 7. Test Closure

## What Is Test Closure?

Test Closure is the final phase of the testing process in which testing activities are reviewed, completed, documented, and formally closed.

It ensures that the testing team has recorded the results, defects, and lessons learned.

### Objectives of Test Closure

1. Verify that planned testing activities are completed.
2. Review test execution results.
3. Check the status of reported defects.
4. Prepare test summary reports.
5. Document lessons learned.
6. Archive important testing documents.
7. Identify areas for improvement.

### Activities Performed During Test Closure

**1. Verify Test Completion**

Check whether all planned test cases have been executed or their remaining status has been documented.

**2. Review Test Results**

Analyze passed, failed, blocked, and not-executed test cases.

**3. Review Defects**

Check:
- Total defects reported.
- Defects fixed.
- Defects still open.
- Defects deferred.
- Reopened defects.

**4. Prepare Test Summary Report**

Create a report containing the overall testing results.

**5. Document Lessons Learned**

Record:
- What went well?
- What problems occurred?
- What could be improved?
- What should be done differently next time?

**6. Archive Testing Documents**

Store test cases, test reports, defect reports, and other relevant documents for future reference.

### Test Summary Report Example

**Project:** E-commerce Application

**Testing Type:** Functional Testing

**Total Test Cases:** 100

| Test Execution Status | Count |
|---|---:|
| Passed | 85 |
| Failed | 10 |
| Blocked | 3 |
| Not Executed | 2 |
| Total | 100 |

**Defect Summary:**

| Defect Status | Count |
|---|---:|
| Total Defects Reported | 10 |
| Fixed and Verified | 7 |
| Open | 2 |
| Deferred | 1 |

**Overall Testing Summary:**

Testing was completed for the planned functional scope. Most test cases passed, while some defects remained open or deferred.

The final release decision should consider the remaining defects, business risks, acceptance criteria, and stakeholder approval.

### Benefits of Test Closure

- Provides a clear record of testing activities.
- Helps evaluate testing effectiveness.
- Improves future testing processes.
- Supports release decisions.
- Preserves project knowledge.
- Helps identify process improvements.

---

# 8. Difference Between Important Testing Terms

## Use Case vs Test Scenario vs Test Case

| Use Case | Test Scenario | Test Case |
|---|---|---|
| Describes user-system interaction | Describes what needs to be tested | Describes how to test |
| Focuses on user goals | Focuses on test conditions | Focuses on execution details |
| Example: User login | Verify login functionality | Enter valid credentials and click Login |

## Test Scenario vs Test Condition

| Test Scenario | Test Condition |
|---|---|
| High-level situation to test | Specific aspect or rule to verify |
| Describes a testing situation | Describes an item or requirement that needs verification |
| Example: Test login functionality | Verify that the password field rejects empty input |

## Test Case vs Test Script

| Test Case | Test Script |
|---|---|
| Contains testing instructions and expected results | Contains instructions or code used to execute tests |
| Can be manual or automated | Often associated with automated execution, though scripts can also be manual |
| Written for verification | Written to perform or automate execution |

## Test Execution vs Test Closure

| Test Execution | Test Closure |
|---|---|
| Runs test cases | Completes and reviews testing activities |
| Records actual results | Prepares final testing reports |
| Identifies defects | Reviews defect status |
| Happens during testing | Happens at the end of the testing cycle |

---

# 9. Practical Example: E-commerce Application

Let's understand the complete testing process using an online shopping application.

## Step 1: Understand the Requirement

Requirement:

A registered customer should be able to log in, search for products, add products to the cart, and complete an order.

## Step 2: Identify Use Cases

- User Login
- Search Product
- View Product Details
- Add Product to Cart
- Remove Product from Cart
- Checkout
- Make Payment
- View Order Confirmation

## Step 3: Create Test Scenarios

For the Add to Cart functionality:

1. Verify adding a product to the cart.
2. Verify adding multiple products.
3. Verify updating product quantity.
4. Verify removing a product.
5. Verify cart total calculation.
6. Verify cart behavior when no product is selected.

## Step 4: Write Test Cases

**Test Case ID:** TC_CART_001

**Title:** Verify that a user can add a product to the cart.

**Precondition:** User is logged in and a product is available.

**Steps:**
1. Open the application.
2. Search for a product.
3. Open product details.
4. Click Add to Cart.
5. Open the shopping cart.

**Expected Result:** The selected product should appear in the shopping cart with the correct details.

## Step 5: Prepare Test Environment

- Install or access the required application build.
- Configure the QA environment.
- Check browser compatibility.
- Prepare test accounts.
- Prepare product and payment test data.

## Step 6: Execute Test Cases

Run each test case and record:
- Expected result.
- Actual result.
- Execution status.

## Step 7: Report Defects

Suppose the cart displays the wrong product price.

Create a defect report with:
- Defect title.
- Reproduction steps.
- Expected result.
- Actual result.
- Severity and priority.
- Screenshot or recording.

## Step 8: Retest and Regression Testing

After the developer fixes the price calculation:

- Retest the reported defect.
- Check whether the cart total is correct.
- Perform relevant regression testing on checkout and payment calculations.

## Step 9: Test Closure

- Review test execution results.
- Review open defects.
- Prepare the test summary report.
- Record lessons learned.
- Archive testing documents.

This is how a manual tester works through a practical testing cycle.

---

# 10. Interview Questions and Answers

### Q1. What are Test Design Techniques?

Test Design Techniques are systematic methods used to identify test conditions and create effective test cases.

### Q2. What is Equivalence Partitioning?

Equivalence Partitioning divides input data into groups that are expected to behave similarly. A representative value from each group is selected for testing.

### Q3. What is Boundary Value Analysis?

Boundary Value Analysis is a testing technique that checks values at and around the minimum and maximum limits of an input range.

### Q4. What is Decision Table Testing?

Decision Table Testing is used to test combinations of conditions and their corresponding actions. It is especially useful for business rules.

### Q5. What is a Use Case?

A Use Case describes how an actor interacts with a system to achieve a particular goal.

### Q6. What is a Test Scenario?

A Test Scenario is a high-level description of a functionality or situation that needs to be tested.

### Q7. What is a Test Case?

A Test Case is a documented set of steps, input data, preconditions, and expected results used to verify application behavior.

### Q8. What is the difference between a Test Scenario and a Test Case?

A Test Scenario describes what needs to be tested, whereas a Test Case describes how to test it using detailed steps and expected results.

### Q9. What is a Test Environment?

A Test Environment is the combination of hardware, software, network, database, tools, and configurations required to execute testing.

### Q10. What is Test Execution?

Test Execution is the process of running test cases, comparing actual results with expected results, and recording their status.

### Q11. What is a Defect Report?

A Defect Report is a document that describes an identified software problem, including reproduction steps, expected and actual results, severity, priority, and supporting evidence.

### Q12. What is the Defect Life Cycle?

The Defect Life Cycle describes the stages a defect passes through, from identification and reporting to fixing, verification, and closure.

### Q13. What is the difference between Severity and Priority?

Severity measures the impact of a defect on the application, while Priority indicates how urgently it should be fixed.

### Q14. What is Test Closure?

Test Closure is the final testing phase in which test results, defects, reports, documentation, and lessons learned are reviewed and finalized.

### Q15. What is a Test Summary Report?

A Test Summary Report is a document that provides an overview of testing activities, test execution results, defects, coverage, and remaining risks.

### Q16. What is the difference between Retesting and Regression Testing?

Retesting verifies whether a previously reported defect has been fixed. Regression Testing checks whether changes have affected existing functionality.

---

# 11. Practical Assignments

Complete these assignments to improve your manual testing skills.

## Assignment 1: Login Page

Write at least 15 test scenarios for a login page.

Include:
- Positive scenarios.
- Negative scenarios.
- UI scenarios.
- Boundary scenarios.
- Security-related scenarios.

## Assignment 2: Test Case Writing

Write at least 10 detailed test cases for:
- Login.
- Registration.
- Forgot Password.

Include all important test case fields.

## Assignment 3: Test Design Techniques

Apply the following techniques to an age input field that accepts values from 18 to 60:

1. Equivalence Partitioning.
2. Boundary Value Analysis.

Write the selected test inputs and expected results.

## Assignment 4: Defect Reporting

Imagine that the Login button does not respond when clicked.

Create a complete defect report containing:
- Defect ID.
- Title.
- Description.
- Steps to Reproduce.
- Expected Result.
- Actual Result.
- Severity.
- Priority.
- Environment.

## Assignment 5: E-commerce Testing

Prepare test scenarios and test cases for:
- Product Search.
- Add to Cart.
- Remove from Cart.
- Checkout.
- Payment.
- Order Confirmation.

## Assignment 6: Test Summary Report

Create a test summary report for an application with:

- Total Test Cases: 50
- Passed: 40
- Failed: 5
- Blocked: 3
- Not Executed: 2

Calculate the pass percentage and write a short testing summary.

---

# 12. Chapter Summary

In this chapter, we learned:

- Test Design Techniques help create effective test cases.
- Equivalence Partitioning divides input data into groups.
- Boundary Value Analysis checks values around boundaries.
- Decision Table Testing checks combinations of conditions.
- State Transition Testing checks changes between application states.
- Use Cases describe user interactions with a system.
- Test Scenarios describe what needs to be tested.
- Test Cases describe how to test a particular condition.
- Test Environments provide the setup required for testing.
- Test Execution involves running test cases and recording results.
- Defect Reporting documents problems found during testing.
- The Defect Life Cycle describes the stages of a defect.
- Severity measures impact, while Priority measures urgency.
- Test Closure completes and documents testing activities.

## Final Learning Point

A manual tester does much more than click buttons.

A good tester understands requirements, identifies test conditions, designs test cases, prepares test data, executes tests, reports defects, verifies fixes, and documents testing results.

**Remember:**

- Use Case = User interaction.
- Test Scenario = What to test.
- Test Case = How to test.
- Test Execution = Run the test.
- Defect Reporting = Document the problem.
- Test Closure = Complete and review testing.