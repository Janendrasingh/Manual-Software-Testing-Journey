# 📘 Types of Software Testing

Software Testing consists of different testing types, each designed to verify a particular aspect of software quality.

A Manual Software Tester should understand when to use each testing type, how to execute it, and how to identify defects.

In this chapter, we will cover:

1. System Testing
2. GUI Testing
3. Functional Testing
4. Non-Functional Testing
5. Regression Testing
6. Re-Testing
7. Exploratory Testing
8. Ad-hoc Testing
9. Smoke Testing
10. Sanity Testing
11. End-to-End Testing

---

# 1. System Testing

## Definition

**System Testing is a level of software testing in which the complete and integrated application is tested to verify whether it meets the specified requirements.**

In simple words, System Testing means testing the entire application after integrating its individual modules.

It checks whether all application components work correctly together.

### Objectives of System Testing

- Verify complete application functionality.
- Identify system-level defects.
- Check whether requirements are satisfied.
- Verify end-to-end workflows.
- Test interactions between different modules.
- Evaluate functional and non-functional requirements.

### Who Performs System Testing?

Primarily:
- Manual Testers.
- QA Engineers.
- Software Test Engineers.

### Example: E-commerce Application

Suppose a company develops an online shopping application.

The application contains:

- Login Module.
- Product Module.
- Shopping Cart Module.
- Payment Module.
- Order Management Module.
- Profile Module.

A System Tester verifies the complete application.

**Test Scenario:**

Verify whether a registered user can successfully purchase a product.

**Test Steps:**

1. Open the shopping application.
2. Log in using valid credentials.
3. Search for a product.
4. Open the product details.
5. Add the product to the cart.
6. Proceed to checkout.
7. Enter the delivery address.
8. Select a payment method.
9. Complete the payment.
10. Verify order confirmation.

**Expected Result:**

The user should be able to complete the entire purchasing process successfully.

### System Testing Activities

1. Understand system requirements.
2. Prepare system test scenarios.
3. Prepare test cases.
4. Prepare test data.
5. Execute test cases.
6. Report defects.
7. Retest fixed defects.
8. Perform regression testing.

### Advantages

- Tests the complete application.
- Identifies integration and system-level defects.
- Validates business workflows.
- Improves software reliability.

### Disadvantages

- Requires a complete or sufficiently integrated application.
- Can be time-consuming.
- Identifying the exact source of a defect can be difficult.

### Interview Questions

**Q1. What is System Testing?**

System Testing evaluates the complete integrated application against specified requirements.

**Q2. Who performs System Testing?**

Primarily the QA or testing team.

**Q3. What is the main objective of System Testing?**

To verify that the complete application works correctly and meets its specified requirements.

---

# 2. GUI Testing (Graphical User Interface Testing)

## Definition

**GUI Testing is a type of software testing that verifies the graphical user interface of an application, including its visual elements, layout, appearance, and user interactions.**

In simple words, GUI Testing checks whether the application looks and behaves correctly from the user's perspective.

GUI elements include:

- Buttons.
- Text Fields.
- Labels.
- Images.
- Icons.
- Dropdowns.
- Checkboxes.
- Radio Buttons.
- Menus.
- Navigation Links.

### Objectives of GUI Testing

- Verify the appearance of the application.
- Check element alignment.
- Verify font size and colors.
- Check button functionality.
- Verify images and icons.
- Check navigation.
- Ensure consistent user experience.

### Example: Login Page

Suppose you are testing the login page of an application.

You need to verify:

| GUI Element | What to Test |
|---|---|
| Username Field | Correct position, size, and visibility. |
| Password Field | Password should be masked. |
| Login Button | Correct appearance and clickable. |
| Forgot Password | Link should navigate correctly. |
| Logo | Correct image should be displayed. |
| Error Message | Correct text and positioning. |
| Background | Correct color and layout. |

### Practical GUI Test Scenarios

1. Verify that the application logo is visible.
2. Verify that all buttons are properly aligned.
3. Verify that text fields have correct dimensions.
4. Verify that buttons are not overlapping.
5. Verify that dropdown options are displayed correctly.
6. Verify that error messages are readable.
7. Verify that the page works at different screen resolutions.
8. Verify that images load correctly.

### Example

Expected Result:

The Login button should be green and positioned below the password field.

Actual Result:

The Login button appears outside the login form.

Status: FAIL.

This is a GUI defect.

### Types of GUI Testing

**1. Layout Testing**

Checks the positioning and alignment of interface elements.

**2. Visual Testing**

Checks colors, fonts, images, spacing, and appearance.

**3. Navigation Testing**

Checks whether links, buttons, and menus navigate correctly.

**4. Responsive UI Testing**

Checks whether the interface adjusts correctly to different screen sizes.

### Advantages

- Improves user experience.
- Identifies visual defects.
- Ensures interface consistency.
- Helps identify usability problems.

### Disadvantages

- Can be time-consuming.
- Different devices may display elements differently.
- Visual comparisons can sometimes be subjective.

### Interview Questions

**Q1. What is GUI Testing?**

GUI Testing verifies the visual appearance, layout, and interactive elements of an application.

**Q2. Give examples of GUI defects.**

Misaligned buttons, incorrect fonts, overlapping text, missing images, and improperly displayed error messages.

**Q3. What is Responsive UI Testing?**

It checks whether an application's interface adjusts correctly to different screen sizes and devices.

---

# 3. Functional Testing

## Definition

**Functional Testing is a type of software testing that verifies whether an application performs its functions according to the specified requirements.**

In simple words, Functional Testing checks what the application does.

It focuses on application features and business logic.

### Objectives

- Verify application functionality.
- Check business requirements.
- Validate input and output.
- Identify missing functionality.
- Verify calculations and business rules.
- Ensure features work correctly.

### Example: Registration Page

Suppose an application has a registration page.

Functional Testing scenarios:

1. Register with valid details.
2. Register with an invalid email address.
3. Submit the form with empty fields.
4. Register using an already registered email.
5. Check password validation.
6. Verify successful registration.
7. Verify error messages.

### Example Test Case

| Field | Details |
|---|---|
| Test Case ID | TC_REG_001 |
| Test Scenario | Verify registration with valid details. |
| Preconditions | Registration page is accessible. |
| Test Steps | Enter valid details and click Register. |
| Test Data | Valid name, email, and password. |
| Expected Result | Account should be created successfully. |
| Actual Result | To be recorded during execution. |
| Status | Not Executed |

### Common Functional Testing Types

- Unit Testing.
- Integration Testing.
- System Testing.
- Smoke Testing.
- Sanity Testing.
- Regression Testing.
- Acceptance Testing.

These terms represent different testing levels or approaches that may include functional checks.

### Advantages

- Ensures features work as expected.
- Identifies business logic defects.
- Verifies customer requirements.
- Improves application reliability.

### Disadvantages

- Does not necessarily evaluate performance.
- Complete input combinations can be difficult to test.
- Depends heavily on clear requirements.

### Interview Questions

**Q1. What is Functional Testing?**

Functional Testing verifies whether application features work according to specified requirements.

**Q2. Give an example of Functional Testing.**

Checking whether a registered user can successfully log in using valid credentials.

**Q3. What is the difference between Functional and GUI Testing?**

Functional Testing checks whether features work correctly, whereas GUI Testing checks the visual appearance and interface behavior.

---

# 4. Non-Functional Testing

## Definition

**Non-Functional Testing is a type of software testing that evaluates the quality attributes of an application, such as performance, security, usability, reliability, and compatibility.**

In simple words, Functional Testing checks what an application does, whereas Non-Functional Testing checks how well the application performs.

### Objectives

- Evaluate application performance.
- Check security.
- Verify usability.
- Test reliability.
- Check compatibility.
- Evaluate scalability.
- Identify quality-related issues.

### Example: E-commerce Application

Suppose an online shopping application works correctly.

However, when 10,000 users access it simultaneously, the application becomes very slow.

The application may pass Functional Testing but fail Performance Testing.

This is why Non-Functional Testing is important.

## Types of Non-Functional Testing

### 1. Performance Testing

Checks the speed, responsiveness, stability, and resource usage of an application under specified workloads.

Example:

Verify whether the shopping application loads its homepage within the required response time.

### 2. Load Testing

Checks application behavior under an expected workload.

Example:

Verify whether 5,000 users can access the application simultaneously without unacceptable performance degradation.

### 3. Stress Testing

Checks how an application behaves when subjected to workloads beyond its expected operating limits.

Example:

Increase the number of users until the application reaches its performance limits.

### 4. Security Testing

Identifies vulnerabilities and checks whether application data and resources are protected.

Example:

Verify that users cannot access another customer's account by changing a URL.

### 5. Usability Testing

Checks whether an application is easy to understand and use.

Example:

Verify whether a new user can easily find and purchase a product.

### 6. Compatibility Testing

Checks whether an application works correctly across different environments.

Example:

Test a website on:

- Google Chrome.
- Mozilla Firefox.
- Microsoft Edge.
- Windows.
- Android.
- iOS.

### 7. Reliability Testing

Checks whether an application performs consistently over time under specified conditions.

Example:

Verify whether a banking application continues operating reliably during extended usage.

### 8. Scalability Testing

Checks whether an application can handle increasing workloads by adding resources or expanding capacity.

Example:

Verify whether an e-commerce application can support an increase from 1,000 to 10,000 concurrent users.

### 9. Recovery Testing

Checks whether an application can recover from failures.

Example:

Verify whether a banking application recovers correctly after an unexpected server shutdown.

### Functional vs Non-Functional Testing

| Basis | Functional Testing | Non-Functional Testing |
|---|---|---|
| Focus | Application functionality | Quality attributes |
| Objective | Verify what the application does | Verify how well it works |
| Requirements | Functional requirements | Non-functional requirements |
| Examples | Login, Registration, Payment | Performance, Security, Usability |
| Main Concern | Correctness of features | Quality and behavior under different conditions |

### Interview Questions

**Q1. What is Non-Functional Testing?**

It evaluates quality attributes such as performance, security, usability, reliability, and compatibility.

**Q2. What is the difference between Load Testing and Stress Testing?**

Load Testing checks performance under expected workloads, while Stress Testing evaluates behavior beyond expected operating limits.

**Q3. What is Compatibility Testing?**

It verifies whether an application works correctly across different browsers, operating systems, devices, and environments.

---

# 5. Regression Testing

## Definition

**Regression Testing is a type of software testing performed to verify that recent code changes, bug fixes, or enhancements have not negatively affected existing functionality.**

In simple words, Regression Testing checks whether previously working features are still working after changes are made.

### Why Do We Need Regression Testing?

Software applications are frequently updated.

Whenever developers:
- Fix bugs.
- Add new features.
- Modify existing features.
- Update code.
- Change database logic.

There is a possibility that existing functionality may stop working.

Regression Testing helps identify such problems.

### Example: E-commerce Application

Suppose an e-commerce application has the following features:

1. Login.
2. Product Search.
3. Add to Cart.
4. Payment.
5. Order Tracking.

A developer fixes a bug in the Add to Cart functionality.

After the fix, the tester checks:

- Login still works.
- Product Search still works.
- Add to Cart works correctly.
- Cart calculations remain correct.
- Payment still works.
- Order Tracking still works.

The tester performs Regression Testing to ensure the change has not broken existing functionality.

### When Is Regression Testing Required?

1. After bug fixes.
2. After adding new features.
3. After code modifications.
4. After database changes.
5. After application upgrades.
6. After integration of new modules.
7. After changes in configuration.

### Regression Testing Process

```text
       Code Change
            |
            ↓
       Impact Analysis
            |
            ↓
      Select Test Cases
            |
            ↓
      Execute Test Cases
            |
            ↓
      Compare Results
            |
            ↓
       Report Defects
            |
            ↓
          Complete
```

### Types of Regression Testing

**1. Corrective Regression Testing**

Used when requirements have not changed and existing test cases can be reused.

**2. Retest-All Regression Testing**

Executes the complete existing test suite.

**3. Selective Regression Testing**

Executes selected test cases related to the changed functionality and its impact.

**4. Progressive Regression Testing**

Used when requirements or specifications have changed and new test cases are required.

**5. Partial Regression Testing**

Checks the changed component and its interactions with related components.

**6. Complete Regression Testing**

Tests the entire application to identify unintended effects of major changes.

### Advantages

- Protects existing functionality.
- Identifies side effects of code changes.
- Improves release confidence.
- Helps maintain software stability.

### Disadvantages

- Can require significant execution time.
- Large test suites can be expensive to maintain.
- Repetitive manual execution can be inefficient.

### Interview Questions

**Q1. What is Regression Testing?**

Regression Testing verifies that existing functionality continues to work after software changes.

**Q2. When do we perform Regression Testing?**

After bug fixes, feature additions, code modifications, and other changes that may affect existing functionality.

**Q3. Why is Regression Testing important?**

It helps identify unintended side effects caused by software changes.

---

# 6. Re-Testing (Confirmation Testing)

## Definition

**Re-Testing is the process of executing previously failed test cases again after developers fix the reported defects to verify whether the defects have been successfully resolved.**

It is also known as Confirmation Testing.

In simple words, Re-Testing checks whether a particular bug has been fixed.

### Example

Suppose a tester identifies a login defect.

**Original Test:**

Input:
- Username: valid username.
- Password: valid password.

Expected Result:

User should successfully log in.

Actual Result:

Application displays an error message.

Status: FAIL.

The tester reports the defect.

The developer fixes the issue and provides a new build.

The tester executes the same test case again.

Expected Result:

User should successfully log in.

Actual Result:

User successfully logs in.

Status: PASS.

This process is called Re-Testing.

### Re-Testing Process

```text
       Execute Test Case
              |
              ↓
        Test Case Failed
              |
              ↓
        Report the Bug
              |
              ↓
        Developer Fixes
              |
              ↓
        New Build Received
              |
              ↓
        Execute Same Test
              |
              ↓
       Verify Bug Fix
              |
              ↓
          Pass / Fail
```

### When Is Re-Testing Required?

- After a defect is fixed.
- After receiving an updated build.
- When a previously failed scenario needs confirmation.
- When developers provide a fix for a reported issue.

### Advantages

- Confirms whether defects are fixed.
- Prevents unresolved bugs from being overlooked.
- Improves application quality.
- Provides confidence in bug fixes.

### Interview Questions

**Q1. What is Re-Testing?**

Re-Testing means executing previously failed test cases again after a defect has been fixed.

**Q2. What is another name for Re-Testing?**

Confirmation Testing.

**Q3. Does Re-Testing require executing the same test case?**

Yes. The original failed test case is executed again, generally with the same relevant conditions and test data.

---

# 7. Regression Testing vs Re-Testing

This is one of the most important comparisons in Manual Software Testing interviews.

| Basis | Regression Testing | Re-Testing |
|---|---|---|
| Meaning | Checks whether existing functionality is affected by changes. | Checks whether a reported defect has been fixed. |
| Purpose | Identify side effects. | Confirm defect resolution. |
| Test Cases | Existing relevant test cases. | Previously failed test cases. |
| Execution | Can include many test cases. | Focuses on specific defect scenarios. |
| Performed After | Code changes, bug fixes, enhancements. | Defect fixes. |
| Main Focus | Existing functionality. | Specific bug fix. |
| Example | Check login, cart, and payment after a cart fix. | Check whether the original cart defect is fixed. |

### Easy Way to Remember

```text
Re-Testing = Is the reported bug fixed?

Regression Testing = Did the fix break anything else?
```

**Important Interview Point:**

After a developer fixes a bug, testers generally perform Re-Testing first to verify the fix, followed by appropriate Regression Testing to check related existing functionality.

---

# 8. Exploratory Testing

## Definition

**Exploratory Testing is a testing approach in which testers simultaneously learn about the application, design test cases, and execute tests based on their observations and experience.**

In simple words, Exploratory Testing means exploring the application to discover defects without depending entirely on predefined test cases.

It encourages testers to think creatively.

### Objectives

- Discover unexpected defects.
- Understand application behavior.
- Explore different workflows.
- Identify usability problems.
- Find scenarios missed by existing test cases.

### Example: Shopping Application

Suppose you are testing an online shopping application.

Instead of following only predefined test cases, you explore the application.

You try:

1. Adding multiple products to the cart.
2. Changing product quantities repeatedly.
3. Refreshing the page during checkout.
4. Applying multiple discount coupons.
5. Opening the same account in multiple tabs.
6. Navigating backward during payment.
7. Removing products during checkout.

During exploration, you discover that applying two coupons gives an incorrect discount.

You report the defect.

This is Exploratory Testing.

### Characteristics

- Less dependent on predefined test cases.
- Requires analytical thinking.
- Uses tester experience.
- Encourages continuous learning.
- Helps discover unexpected defects.

### Session-Based Exploratory Testing

Exploratory Testing can be organized into time-limited sessions.

A session generally includes:

1. Test Charter – Defines the objective.
2. Time Box – Defines the testing duration.
3. Exploration – Tester explores the application.
4. Notes – Tester records observations.
5. Debrief – Results are reviewed.

### Example Test Charter

```text
Objective:
Explore the shopping cart functionality.

Duration:
60 minutes.

Focus:
- Product quantity.
- Coupon application.
- Cart calculations.
- Product removal.

Expected Outcome:
Identify unexpected behavior and defects.
```

### Advantages

- Finds unexpected defects.
- Encourages creative thinking.
- Helps understand unfamiliar applications.
- Useful when requirements are incomplete.
- Identifies gaps in predefined test cases.

### Disadvantages

- Test coverage can be difficult to measure.
- Results depend on tester skills.
- Reproducing some defects can be difficult.
- Documentation requires discipline.

### Interview Questions

**Q1. What is Exploratory Testing?**

It is an approach in which testers simultaneously learn, design, and execute tests while exploring an application.

**Q2. Is Exploratory Testing completely unplanned?**

No. It may use test charters, objectives, time limits, and documented observations even though detailed test cases are not necessarily prepared in advance.

**Q3. When is Exploratory Testing useful?**

It is especially useful for unfamiliar applications, incomplete requirements, and discovering unexpected defects.

---

# 9. Ad-hoc Testing

## Definition

**Ad-hoc Testing is an informal testing approach performed without predefined test cases or detailed documentation to identify defects through random or experience-based testing.**

In simple words, Ad-hoc Testing means testing an application informally without following a structured test case.

### Objectives

- Discover unexpected defects.
- Identify obvious application problems.
- Find defects through random inputs.
- Check application stability.
- Identify issues missed by formal testing.

### Example: Login Page

Suppose you are testing a login page.

Instead of following written test cases, you try unusual inputs:

- Enter spaces in the username.
- Paste a very long password.
- Click the Login button repeatedly.
- Refresh the page during login.
- Use special characters.
- Open multiple login tabs.
- Submit the form repeatedly.

You discover that clicking the Login button repeatedly creates multiple login requests.

You report the issue.

This is Ad-hoc Testing.

### Characteristics

- No formal test cases.
- Informal execution.
- Relies on tester experience.
- Random or spontaneous inputs.
- Minimal documentation, although defects should still be reported.

### Types of Ad-hoc Testing

**1. Buddy Testing**

Two people work together to test the same functionality, commonly a developer and a tester.

**2. Pair Testing**

Two people test together, typically with one person controlling the testing activity while the other observes and suggests scenarios.

**3. Monkey Testing**

Testing an application with random inputs or actions without following predefined test scenarios.

### Advantages

- Quick to perform.
- Requires minimal preparation.
- Can identify unexpected defects.
- Useful for finding obvious issues.

### Disadvantages

- Test coverage is difficult to measure.
- Results may not be reproducible.
- Depends heavily on tester experience.
- Difficult to track systematically.

### Interview Questions

**Q1. What is Ad-hoc Testing?**

It is informal testing performed without predefined test cases to identify defects.

**Q2. What is Monkey Testing?**

Monkey Testing involves providing random inputs or performing random actions to observe application behavior.

**Q3. Is documentation required in Ad-hoc Testing?**

Formal test cases are not required, but identified defects should be documented and reported.

---

# 10. Exploratory Testing vs Ad-hoc Testing

Both approaches are informal compared with scripted testing, but they are not exactly the same.

| Basis | Exploratory Testing | Ad-hoc Testing |
|---|---|---|
| Meaning | Learning, designing, and executing tests simultaneously. | Informal testing without predefined test cases. |
| Planning | Has objectives or test charters. | Usually has minimal planning. |
| Approach | Structured exploration. | Informal and spontaneous. |
| Documentation | Observations and results are generally recorded. | Documentation is generally minimal. |
| Focus | Discover defects and understand behavior. | Find defects quickly. |
| Tester Skills | Requires analytical and exploratory skills. | Relies heavily on experience and intuition. |

### Easy Way to Remember

```text
Exploratory Testing = Explore with an Objective.

Ad-hoc Testing = Test Informally without a Formal Plan.
```

---

# 11. Smoke Testing

## Definition

**Smoke Testing is a preliminary level of testing performed on a new software build to verify whether the critical functionalities are working and whether the build is stable enough for further testing.**

In simple words, Smoke Testing checks whether the basic features of an application are working before the testing team starts detailed testing.

It is also called Build Verification Testing (BVT) in many contexts.

### Objectives

- Verify build stability.
- Check critical functionalities.
- Identify major defects early.
- Decide whether the build is suitable for further testing.
- Save testing time.

### Example: E-commerce Application

Suppose developers provide a new build of an online shopping application.

Before executing hundreds of test cases, testers perform Smoke Testing.

They check:

1. Application launches successfully.
2. Login functionality works.
3. Homepage loads.
4. Products are displayed.
5. Add to Cart works.
6. Checkout page opens.

If these critical functions work, testers can proceed with detailed testing.

If major functionality is broken, the build may be rejected for further testing.

### Smoke Testing Process

```text
       New Build Received
               |
               ↓
       Install / Deploy Build
               |
               ↓
       Execute Critical Tests
               |
               ↓
        Check Test Results
               |
          -----------
          |         |
         Pass      Fail
          |         |
          ↓         ↓
      Proceed    Reject / Hold
      Testing    Build for Fix
```

### Characteristics

- Broad but shallow testing.
- Covers critical functionalities.
- Performed on a new build.
- Usually performed before detailed testing.
- Helps assess build stability.

### Advantages

- Saves time.
- Identifies major build problems.
- Prevents wasting effort on unstable builds.
- Provides early feedback.

### Disadvantages

- Does not cover detailed functionality.
- Cannot identify all defects.
- Passing Smoke Testing does not mean the application is defect-free.

### Interview Questions

**Q1. What is Smoke Testing?**

Smoke Testing is preliminary testing performed on a new build to verify whether critical functionality works and the build is stable enough for further testing.

**Q2. What is another name for Smoke Testing?**

Build Verification Testing (BVT).

**Q3. When is Smoke Testing performed?**

Generally after receiving and deploying a new build, before detailed testing.

---

# 12. Sanity Testing

## Definition

**Sanity Testing is a focused testing approach performed after minor changes or bug fixes to verify whether the specific affected functionality is working correctly and whether further testing is reasonable.**

In simple words, Sanity Testing checks whether a particular change or fix is working as expected.

### Objectives

- Verify specific changes.
- Check affected functionality.
- Identify obvious defects after minor modifications.
- Avoid unnecessary detailed testing when the change is clearly broken.
- Decide whether further testing should continue.

### Example: E-commerce Application

Suppose a developer fixes a discount calculation bug.

Previously:

Product Price = ₹1,000.

Discount = 10%.

Expected Final Price = ₹900.

Actual Final Price = ₹950.

The developer fixes the calculation logic.

After receiving the updated build, the tester checks:

- Whether the discount is calculated correctly.
- Whether the final price is correct.
- Whether the discount is displayed properly.
- Whether the affected checkout calculation works.

This focused testing is Sanity Testing.

### Characteristics

- Narrow and focused testing.
- Usually performed after minor changes or fixes.
- Covers affected functionality.
- Helps decide whether further testing is worthwhile.
- Does not necessarily cover the complete application.

### Advantages

- Saves time.
- Quickly checks modified functionality.
- Helps identify obvious problems.
- Avoids unnecessary testing of an unusable change.

### Disadvantages

- Limited test coverage.
- Does not verify the entire application.
- May not identify defects in unrelated functionality.

### Interview Questions

**Q1. What is Sanity Testing?**

Sanity Testing is focused testing performed after a minor change or fix to verify that the affected functionality works correctly.

**Q2. When is Sanity Testing performed?**

Generally after receiving a build containing a minor change or bug fix.

**Q3. Does Sanity Testing test the entire application?**

No. It focuses on the affected functionality and closely related areas.

---

# 13. Smoke Testing vs Sanity Testing

This is one of the most frequently asked questions in Manual Software Testing interviews.

| Basis | Smoke Testing | Sanity Testing |
|---|---|---|
| Purpose | Check overall build stability. | Check specific changed functionality. |
| Scope | Broad but shallow. | Narrow and focused. |
| Focus | Critical application features. | Modified or affected features. |
| Performed When | After receiving a new build. | After minor changes or fixes. |
| Objective | Decide whether further testing can begin. | Decide whether further focused testing is worthwhile. |
| Example | Check login, homepage, cart, checkout. | Check a fixed discount calculation. |

### Easy Way to Remember

```text
Smoke Testing = Is the Build Stable?

Sanity Testing = Is the Specific Change Working?
```

**Important Note:** In real projects, teams may use these terms differently. Smoke Testing generally checks build stability, while Sanity Testing generally checks a focused area after a change.

---

# 14. End-to-End Testing (E2E Testing)

## Definition

**End-to-End Testing is a testing approach that verifies a complete business workflow from beginning to end, ensuring that all integrated components and external systems work together correctly.**

In simple words, End-to-End Testing checks whether a complete user journey works from its starting point to its final outcome.

It validates the entire workflow rather than testing only individual features.

### Objectives

- Verify complete business workflows.
- Check communication between integrated systems.
- Validate data flow.
- Identify integration defects.
- Verify real-world user journeys.
- Ensure the complete process works correctly.

### Example: Online Shopping Application

Consider a customer purchasing a mobile phone online.

The complete workflow includes:

**Step 1: User Login**

The customer logs into the application.

**Step 2: Product Search**

The customer searches for a mobile phone.

**Step 3: Product Selection**

The customer selects a product.

**Step 4: Add to Cart**

The product is added to the shopping cart.

**Step 5: Checkout**

The customer enters the delivery address.

**Step 6: Payment**

The customer completes the payment.

**Step 7: Order Confirmation**

The system generates an order ID.

**Step 8: Inventory Update**

The product inventory is updated.

**Step 9: Notification**

The customer receives an order confirmation notification.

**Step 10: Order Tracking**

The customer tracks the order.

The tester verifies the entire journey.

### End-to-End Testing Diagram

```text
          User Login
              |
              ↓
         Product Search
              |
              ↓
        Product Selection
              |
              ↓
           Add to Cart
              |
              ↓
           Checkout
              |
              ↓
            Payment
              |
              ↓
       Order Confirmation
              |
              ↓
       Inventory Update
              |
              ↓
        Email / SMS Alert
              |
              ↓
         Order Tracking
              |
              ↓
             END
```

### What Does E2E Testing Verify?

- User interactions.
- Frontend functionality.
- Backend processing.
- Database operations.
- API communication.
- External integrations.
- Data consistency.
- Complete business workflows.

### Types of End-to-End Testing

**1. Horizontal E2E Testing**

Tests a complete business workflow across different application modules.

Example:

Login → Product Search → Cart → Payment → Order Confirmation.

**2. Vertical E2E Testing**

Tests a specific functionality through multiple technical layers.

Example:

Testing a payment request from the user interface through the API and backend service to database processing.

### Advantages

- Validates real-world workflows.
- Identifies integration problems.
- Checks complete business processes.
- Improves release confidence.

### Disadvantages

- Can be time-consuming.
- Requires a stable test environment.
- Test execution may depend on external services.
- Defect investigation can be difficult.
- Maintaining E2E test scenarios can be expensive.

### Interview Questions

**Q1. What is End-to-End Testing?**

It verifies a complete business workflow from beginning to end across integrated application components.

**Q2. Give an example of E2E Testing.**

Testing the complete online shopping process, from user login to product purchase and order confirmation.

**Q3. What is the difference between System Testing and E2E Testing?**

System Testing evaluates the complete application against system requirements, whereas E2E Testing specifically verifies complete user or business workflows across integrated components and systems.

---

# 15. Comparison of Important Testing Types

| Testing Type | Main Purpose | Example |
|---|---|---|
| System Testing | Test complete application | Test complete shopping application |
| GUI Testing | Check visual interface | Check button alignment |
| Functional Testing | Verify features | Test login functionality |
| Non-Functional Testing | Verify quality attributes | Test application performance |
| Regression Testing | Check existing functionality after changes | Test login and payment after cart changes |
| Re-Testing | Confirm bug fix | Execute previously failed login test |
| Exploratory Testing | Discover unexpected defects | Explore different checkout scenarios |
| Ad-hoc Testing | Informal testing | Enter random inputs |
| Smoke Testing | Check build stability | Verify critical application features |
| Sanity Testing | Check specific changes | Verify fixed discount calculation |
| E2E Testing | Verify complete workflow | Test purchase from login to order tracking |

---

# 16. Important Interview Questions and Answers

### Q1. What are the different types of Software Testing?

Some important types include Functional Testing, Non-Functional Testing, GUI Testing, Regression Testing, Re-Testing, Exploratory Testing, Ad-hoc Testing, Smoke Testing, Sanity Testing, System Testing, and End-to-End Testing.

### Q2. What is the difference between System Testing and End-to-End Testing?

System Testing checks the complete application against its requirements. End-to-End Testing checks complete business workflows across integrated components and systems.

### Q3. What is the difference between Functional and Non-Functional Testing?

Functional Testing checks what an application does, while Non-Functional Testing checks how well it performs.

### Q4. What is the difference between Regression Testing and Re-Testing?

Regression Testing checks whether existing functionality is affected by changes. Re-Testing verifies whether a specific reported defect has been fixed.

### Q5. What is the difference between Smoke and Sanity Testing?

Smoke Testing checks critical functionality and overall build stability. Sanity Testing focuses on specific changes or fixes.

### Q6. What is the difference between Exploratory and Ad-hoc Testing?

Exploratory Testing involves learning, designing, and executing tests simultaneously with an objective. Ad-hoc Testing is more informal and generally lacks a defined testing structure.

### Q7. What is GUI Testing?

GUI Testing verifies the visual elements, layout, appearance, and interactions of an application.

### Q8. What is Performance Testing?

Performance Testing evaluates application responsiveness, speed, stability, and resource usage under specified workloads.

### Q9. Can Regression Testing be automated?

Yes. Regression Testing is commonly automated to reduce repetitive manual effort, although manual regression testing is also used.

### Q10. Is Smoke Testing performed before Sanity Testing?

Not necessarily. They serve different purposes and their order depends on the project workflow. Smoke Testing commonly checks a new build before detailed testing, while Sanity Testing checks a focused change.

### Q11. What is Confirmation Testing?

Confirmation Testing is another name for Re-Testing. It verifies whether a reported defect has been fixed.

### Q12. What is Monkey Testing?

Monkey Testing involves performing random actions or providing random inputs to identify unexpected application behavior.

### Q13. What is the main purpose of End-to-End Testing?

To verify that complete business workflows work correctly across all integrated components and systems.

---

# 17. Practical Assignments

Use an online shopping application as your testing project.

Complete the following exercises.

## Assignment 1: Functional Testing

Prepare 10 test scenarios for:

- Login.
- Registration.
- Product Search.
- Add to Cart.
- Checkout.

## Assignment 2: GUI Testing

Identify at least 10 GUI test scenarios for a login page.

Consider:

- Alignment.
- Colors.
- Fonts.
- Buttons.
- Text fields.
- Images.
- Error messages.
- Responsiveness.

## Assignment 3: Regression vs Re-Testing

Scenario:

A developer fixes a bug in the payment module.

Answer:

1. Which test should be performed to confirm the bug fix?
2. Which test should be performed to check whether other features still work?
3. Give three examples of related regression test cases.

## Assignment 4: Smoke Testing

A new build of an e-commerce application has been received.

Prepare five critical Smoke Test cases.

## Assignment 5: Sanity Testing

A developer fixes the product discount calculation.

Prepare five focused test cases to verify the change.

## Assignment 6: Exploratory Testing

Explore an application's shopping cart without using predefined test cases.

Try:

- Adding multiple products.
- Removing products.
- Changing quantities.
- Applying coupons.
- Refreshing the page.
- Navigating backward.

Record any unexpected behavior.

## Assignment 7: Ad-hoc Testing

Perform informal testing on a login page.

Try unusual inputs and interactions.

Document the defects you discover.

## Assignment 8: End-to-End Testing

Prepare a complete test scenario for:

User Login → Product Search → Add to Cart → Checkout → Payment → Order Confirmation.

Verify that the complete workflow works correctly.

---

# 18. Chapter Summary

| Topic | Key Learning |
|---|---|
| System Testing | Tests the complete integrated application. |
| GUI Testing | Checks visual interface and interactions. |
| Functional Testing | Checks application functionality. |
| Non-Functional Testing | Checks performance and quality attributes. |
| Regression Testing | Checks existing functionality after changes. |
| Re-Testing | Confirms whether a reported defect is fixed. |
| Exploratory Testing | Simultaneously learns, designs, and executes tests. |
| Ad-hoc Testing | Informal testing without predefined test cases. |
| Smoke Testing | Checks critical functionality of a new build. |
| Sanity Testing | Checks specific changes or fixes. |
| E2E Testing | Tests complete business workflows. |

---

# ✅ Chapter Completion Checklist

- [ ] Understand System Testing.
- [ ] Understand GUI Testing.
- [ ] Understand Functional Testing.
- [ ] Understand Non-Functional Testing.
- [ ] Learn Performance, Load, and Stress Testing.
- [ ] Understand Regression Testing.
- [ ] Understand Re-Testing.
- [ ] Differentiate Regression and Re-Testing.
- [ ] Understand Exploratory Testing.
- [ ] Understand Ad-hoc Testing.
- [ ] Differentiate Exploratory and Ad-hoc Testing.
- [ ] Understand Smoke Testing.
- [ ] Understand Sanity Testing.
- [ ] Differentiate Smoke and Sanity Testing.
- [ ] Understand End-to-End Testing.
- [ ] Complete practical assignments.
- [ ] Prepare interview questions.

---

**Previous Topic:** QA, QC, QE and Testing Fundamentals.

**Next Topic:** Test Case Design Techniques – Equivalence Partitioning, Boundary Value Analysis, Decision Table Testing, and State Transition Testing.

**Learning Philosophy:** Understand the concept → Learn the purpose → Practice with real-world scenarios → Identify differences → Prepare for interviews.