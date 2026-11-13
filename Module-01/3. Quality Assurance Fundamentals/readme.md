# 📘 QA, QC, QE and Testing Fundamentals

This chapter covers important Software Testing concepts, including Quality Assurance (QA), Quality Control (QC), Quality Engineering (QE), Verification, Validation, Testing Levels, White Box Testing, Black Box Testing, Static Testing, and Dynamic Testing.

Understanding these concepts helps testers understand their responsibilities and how software quality is maintained throughout the Software Development Life Cycle (SDLC).

---

# 1. QA vs QC vs QE

QA, QC, and QE are three important concepts related to software quality.

Although they are closely related, their approaches and responsibilities are different.

## 1.1 What is QA (Quality Assurance)?

### Definition

**Quality Assurance (QA) is a process-oriented approach that focuses on preventing defects by improving the processes used to develop software.**

In simple words, QA ensures that the right processes are followed to develop quality software.

QA focuses on preventing defects rather than simply finding them.

### Objectives of QA

- Prevent defects during development.
- Improve software development processes.
- Establish quality standards.
- Ensure teams follow defined procedures.
- Improve development efficiency.
- Reduce the chances of defects.

### QA Activities

1. Reviewing software development processes.
2. Preparing quality standards.
3. Conducting process audits.
4. Reviewing requirement documents.
5. Establishing testing procedures.
6. Monitoring compliance with processes.
7. Improving development practices.

### Example

Suppose a company frequently receives complaints about incorrect login functionality.

The QA team investigates the development process and discovers that requirements are not being reviewed properly.

The QA team introduces a requirement review process before development begins.

This helps prevent similar defects in future releases.

**Remember:** QA focuses on preventing defects by improving processes.

---

## 1.2 What is QC (Quality Control)?

### Definition

**Quality Control (QC) is a product-oriented approach that focuses on identifying defects in the actual software product.**

In simple words, QC checks whether the developed software meets the required quality standards.

QC focuses on detecting defects.

### Objectives of QC

- Identify defects.
- Verify software functionality.
- Check whether requirements are satisfied.
- Ensure the product meets quality standards.
- Reduce defects before release.

### QC Activities

1. Executing test cases.
2. Performing functional testing.
3. Performing regression testing.
4. Identifying bugs.
5. Reporting defects.
6. Retesting fixed defects.
7. Verifying actual results against expected results.

### Example

Suppose a tester checks a login page.

Test scenarios:

- Login with valid credentials.
- Login with invalid credentials.
- Login with empty fields.
- Login with an incorrect password.

The tester identifies that the application allows login with an incorrect password.

The tester reports the defect to the developer.

This is a QC activity.

**Remember:** QC focuses on identifying defects in the product.

---

## 1.3 What is QE (Quality Engineering)?

### Definition

**Quality Engineering (QE) is an engineering-driven approach that integrates quality practices throughout the software development life cycle using tools, automation, engineering principles, and continuous improvement.**

In simple words, QE focuses on building quality into the software development process rather than depending only on testing at the end.

QE combines prevention, detection, automation, and continuous quality improvement.

### Objectives of QE

- Build quality into every development stage.
- Automate repetitive testing activities.
- Improve testing efficiency.
- Integrate testing into CI/CD pipelines.
- Identify risks early.
- Improve software reliability.
- Promote continuous quality improvement.

### QE Activities

1. Designing automated testing frameworks.
2. Integrating automated tests into CI/CD pipelines.
3. Performing API and performance testing.
4. Implementing continuous testing.
5. Monitoring application quality.
6. Improving test coverage.
7. Supporting developers with quality engineering practices.

### Example

Suppose a company develops an e-commerce application.

The QE team:
- Creates automated regression tests.
- Integrates tests into the CI/CD pipeline.
- Runs tests whenever developers submit code.
- Identifies failures automatically.
- Monitors application performance.

This helps identify problems earlier and improves release confidence.

**Remember:** QE uses engineering practices and automation to build quality throughout the development process.

---

## QA vs QC vs QE Comparison

| Basis | QA | QC | QE |
|---|---|---|---|
| Full Form | Quality Assurance | Quality Control | Quality Engineering |
| Focus | Process | Product | Engineering and quality practices |
| Approach | Preventive | Detective | Preventive and continuous |
| Objective | Prevent defects | Identify defects | Build and maintain quality |
| Activities | Process reviews, audits | Test execution, defect reporting | Automation, CI/CD, continuous testing |
| Responsibility | Quality processes | Product quality checks | Quality across development |
| Example | Reviewing requirements | Testing login functionality | Automating login regression tests |

### Easy Way to Remember

```text
QA = Prevent Defects
QC = Detect Defects
QE = Engineer Quality
```

### Interview Questions

**Q1. What is the difference between QA and QC?**

QA is process-oriented and focuses on preventing defects, whereas QC is product-oriented and focuses on identifying defects.

**Q2. Is testing part of QA or QC?**

Software testing is generally considered a QC activity because it evaluates the actual product to identify defects. It also contributes to the broader QA objective of improving quality.

**Q3. What is Quality Engineering?**

Quality Engineering integrates engineering practices, automation, continuous testing, and quality processes throughout software development.

---

# 2. Verification vs Validation

Verification and Validation are two important software quality activities.

Both help ensure that software meets requirements and user expectations.

## 2.1 What is Verification?

### Definition

**Verification is the process of checking whether software work products meet specified requirements and design specifications.**

In simple words, verification checks whether we are building the product correctly.

### Main Question

**Are we building the product right?**

### Characteristics of Verification

- Focuses on documents, requirements, and design.
- Helps identify defects early.
- Usually performed without executing the application.
- Includes reviews and inspections.
- Takes place throughout development.

### Verification Activities

1. Requirement Reviews.
2. Design Reviews.
3. Code Reviews.
4. Document Inspections.
5. Walkthroughs.
6. Technical Reviews.

### Example

Suppose a customer requires a login page with:

- Username field.
- Password field.
- Login button.
- Forgot Password option.

During verification, the team reviews the requirement document and design to check whether all specified elements are included.

The application does not need to be executed for this review.

---

## 2.2 What is Validation?

### Definition

**Validation is the process of evaluating software to determine whether it satisfies user needs and intended requirements.**

In simple words, validation checks whether we are building the right product.

### Main Question

**Are we building the right product?**

### Characteristics of Validation

- Focuses on the actual software.
- Usually involves executing the application.
- Checks functionality and behavior.
- Identifies defects during testing.
- Confirms that the software meets user expectations.

### Validation Activities

1. Unit Testing.
2. Integration Testing.
3. System Testing.
4. Acceptance Testing.
5. Functional Testing.
6. Usability Testing.

### Example

Suppose a login page has been developed.

The tester:
- Enters valid credentials.
- Enters invalid credentials.
- Leaves fields empty.
- Clicks the Login button.

The tester checks whether the application behaves according to requirements.

This is validation.

---

## Verification vs Validation Comparison

| Basis | Verification | Validation |
|---|---|---|
| Meaning | Checks work products against specifications. | Checks whether software meets user needs. |
| Main Question | Are we building the product right? | Are we building the right product? |
| Approach | Static activities. | Generally dynamic activities. |
| Execution | Usually does not require executing software. | Usually involves executing software. |
| Activities | Reviews, inspections, walkthroughs. | Unit, Integration, System, Acceptance Testing. |
| Objective | Prevent defects early. | Identify defects and confirm suitability. |
| Example | Reviewing requirement documents. | Executing login test cases. |

### Easy Way to Remember

```text
Verification = Without Executing Software
Validation   = By Evaluating Running Software
```

**Important:** Verification is commonly performed through static techniques, while validation generally involves dynamic testing. However, validation is broader than just executing test cases.

### Interview Questions

**Q1. What is Verification?**

Verification checks whether software work products meet specified requirements and design specifications.

**Q2. What is Validation?**

Validation checks whether the developed software satisfies user needs and intended requirements.

**Q3. Can verification be performed without executing software?**

Yes. Verification commonly uses reviews, inspections, walkthroughs, and other static techniques.

**Q4. Give a real-world example of Verification and Validation.**

Reviewing a login page requirement document is verification, while executing login test cases is validation.

---

# 3. Different Levels of Software Testing

Software Testing Levels describe different stages at which software is tested.

The main objective is to identify defects at different levels, starting from individual components and moving towards the complete application.

There are four commonly recognized levels of software testing:

1. Unit Testing.
2. Integration Testing.
3. System Testing.
4. Acceptance Testing.

## 3.1 Unit Testing

### Definition

**Unit Testing is the process of testing individual components or units of software independently to verify that they work correctly.**

A unit can be:
- Function.
- Method.
- Class.
- Module.
- Component.

### Who Performs Unit Testing?

Primarily developers.

### Objectives

- Identify defects in individual components.
- Verify business logic.
- Check calculations.
- Ensure functions work correctly.
- Identify coding mistakes early.

### Example

Consider an application that calculates the total price of products.

```javascript
function calculateTotal(price, quantity) {
    return price * quantity;
}

console.log(calculateTotal(100, 5));
```

Expected Output:

```text
500
```

A developer tests this function independently to verify whether it calculates the total correctly.

This is Unit Testing.

### Common Unit Testing Tools

- JUnit.
- TestNG.
- NUnit.
- Jest.

---

## 3.2 Integration Testing

### Definition

**Integration Testing is the process of testing two or more integrated modules to verify whether they communicate and work together correctly.**

Individual modules may work properly, but problems can occur when they interact.

### Who Performs Integration Testing?

Developers and testers, depending on the project and organization.

### Objectives

- Identify interface defects.
- Verify communication between modules.
- Check data transfer.
- Verify API interactions.
- Identify integration issues.

### Example

Consider an online shopping application.

It contains:

1. Login Module.
2. Product Module.
3. Shopping Cart Module.
4. Payment Module.

Each module may work independently.

However, when a user adds a product to the cart and proceeds to payment, integration problems may occur.

The tester checks whether:
- Product details transfer correctly to the cart.
- Cart total reaches the payment module.
- Payment status updates the order.

This is Integration Testing.

### Types of Integration Testing

**1. Top-Down Integration Testing**

Testing begins with higher-level modules and gradually integrates lower-level modules.

**2. Bottom-Up Integration Testing**

Testing begins with lower-level modules and gradually integrates higher-level modules.

**3. Big Bang Integration Testing**

Multiple modules are integrated together and tested as a complete group.

**4. Sandwich (Hybrid) Integration Testing**

Combines Top-Down and Bottom-Up integration approaches.

---

## 3.3 System Testing

### Definition

**System Testing is the process of testing the complete and integrated software application to verify whether it meets specified system requirements.**

It evaluates the application as a whole.

### Who Performs System Testing?

Primarily the testing or QA team.

### Objectives

- Verify complete application functionality.
- Identify system-level defects.
- Check end-to-end workflows.
- Verify functional and non-functional requirements.
- Ensure the system works as expected.

### Example

Consider an online shopping application.

The tester checks the complete shopping journey:

1. Register an account.
2. Log in.
3. Search for a product.
4. Add the product to the cart.
5. Enter the delivery address.
6. Make payment.
7. Receive order confirmation.

If the complete workflow works correctly, the application passes that system test scenario.

### Types of System Testing

- Functional Testing.
- Performance Testing.
- Security Testing.
- Usability Testing.
- Compatibility Testing.
- Recovery Testing.
- Reliability Testing.

---

## 3.4 Acceptance Testing

### Definition

**Acceptance Testing is the process of evaluating software to determine whether it satisfies business requirements and is acceptable for delivery or use.**

It is generally performed before the software is accepted or released.

### Who Performs Acceptance Testing?

Depending on the project:
- Customers.
- End Users.
- Business Representatives.
- Client Representatives.
- Dedicated Acceptance Testers.

### Objectives

- Confirm business requirements.
- Validate user expectations.
- Verify business workflows.
- Determine release readiness.
- Obtain customer acceptance.

### Types of Acceptance Testing

**1. User Acceptance Testing (UAT)**

Actual users or their representatives verify whether the application meets business needs.

Example:

Employees test a newly developed attendance management application before the company starts using it.

**2. Alpha Testing**

Testing performed at the developer's site or controlled environment before the product is made available to external users.

**3. Beta Testing**

Testing performed by selected external users in real-world environments before wider release.

**4. Operational Acceptance Testing (OAT)**

Checks whether the software is ready for operational use.

It may cover:
- Backup and recovery.
- Installation.
- Monitoring.
- Maintenance.
- Operational procedures.

---

## Software Testing Levels Diagram

```text
          Acceptance Testing
                  |
                  ↓
             System Testing
                  |
                  ↓
           Integration Testing
                  |
                  ↓
              Unit Testing
```

**Understanding the Diagram:**

- Unit Testing checks individual components.
- Integration Testing checks interactions between components.
- System Testing checks the complete application.
- Acceptance Testing checks whether the application meets business needs.

## Comparison of Testing Levels

| Basis | Unit | Integration | System | Acceptance |
|---|---|---|---|---|
| Scope | Individual unit | Connected modules | Complete application | Business requirements |
| Performed By | Developers | Developers/Testers | Testers | Customers/Users |
| Main Objective | Check individual logic | Check module communication | Check overall system | Confirm business acceptance |
| Example | Test price calculation | Cart and payment integration | Complete shopping workflow | Customer approval |

### Interview Questions

**Q1. What are the four levels of software testing?**

Unit Testing, Integration Testing, System Testing, and Acceptance Testing.

**Q2. Who performs Unit Testing?**

Primarily developers.

**Q3. What is Integration Testing?**

It checks whether integrated modules communicate and function correctly.

**Q4. What is System Testing?**

It tests the complete integrated application against specified requirements.

**Q5. What is UAT?**

User Acceptance Testing is performed by users or their representatives to verify whether the application satisfies business needs.

**Q6. What is the difference between Alpha and Beta Testing?**

Alpha Testing is performed in a controlled environment, generally at the developer's site, while Beta Testing involves selected external users testing the software in real-world conditions.

---

# 4. White Box Testing

## Definition

**White Box Testing is a software testing technique in which the internal structure, source code, logic, and execution paths of an application are examined.**

It is also known as:
- Clear Box Testing.
- Glass Box Testing.
- Structural Testing.
- Code-Based Testing.

In simple words, White Box Testing means testing the internal working of software.

### Who Performs White Box Testing?

Primarily:
- Developers.
- Automation Engineers.
- Technical Test Engineers.

### Objectives

- Verify internal logic.
- Identify coding errors.
- Check execution paths.
- Verify conditions and loops.
- Improve code coverage.
- Identify security weaknesses in code.

### Example

Consider the following code:

```javascript
function checkAge(age) {

    if (age >= 18) {
        return "Eligible";
    } else {
        return "Not Eligible";
    }

}
```

A White Box Tester examines the internal code and tests both conditions.

Test Case 1:

```text
Input: 20
Expected Output: Eligible
```

Test Case 2:

```text
Input: 15
Expected Output: Not Eligible
```

The tester checks whether both branches execute correctly.

### White Box Testing Techniques

**1. Statement Coverage**

Checks whether every executable statement in the code has been executed at least once.

**2. Branch Coverage**

Checks whether each possible branch or decision outcome has been executed.

**3. Condition Coverage**

Checks whether each individual Boolean condition has been evaluated as both True and False.

**4. Path Coverage**

Checks different execution paths through the code.

### Advantages

- Identifies internal coding defects.
- Helps improve code quality.
- Detects logical errors.
- Helps identify unnecessary code.
- Supports security analysis.

### Disadvantages

- Requires programming knowledge.
- Can be time-consuming.
- Testing complex code can be difficult.
- Complete path coverage may be impractical for complex applications.

### Common Tools

- JUnit.
- JaCoCo.
- SonarQube.
- NUnit.
- Jest.

---

# 5. Black Box Testing

## Definition

**Black Box Testing is a testing technique in which software functionality is tested without knowing or examining its internal source code or implementation details.**

In simple words, testers provide inputs and verify whether the application produces the expected outputs.

The tester focuses on what the application does rather than how it works internally.

### Who Performs Black Box Testing?

- Manual Testers.
- QA Engineers.
- Automation Testers.

### Objectives

- Verify application functionality.
- Identify missing features.
- Check input and output behavior.
- Validate business requirements.
- Identify user-facing defects.

### Example

Consider a login page.

The tester does not need to understand the source code.

The tester checks:

| Test Input | Expected Result |
|---|---|
| Valid username and password | Login successful |
| Invalid password | Error message |
| Empty username | Validation message |
| Empty password | Validation message |
| Both fields empty | Required field messages |

This is Black Box Testing.

### Black Box Testing Techniques

**1. Equivalence Partitioning**

Divides input data into groups or partitions that are expected to behave similarly.

Example:

Suppose an application accepts ages between 18 and 60.

Partitions:

- Below 18: Invalid.
- 18–60: Valid.
- Above 60: Invalid.

**2. Boundary Value Analysis**

Tests values at and around the boundaries of input ranges.

For the age range 18–60:

| Test Value | Expected Result |
|---|---|
| 17 | Invalid |
| 18 | Valid |
| 19 | Valid |
| 59 | Valid |
| 60 | Valid |
| 61 | Invalid |

**3. Decision Table Testing**

Uses a table to test combinations of conditions and their corresponding actions.

Example:

A user can log in only when the username and password are correct.

| Username | Password | Expected Result |
|---|---|---|
| Valid | Valid | Login Successful |
| Valid | Invalid | Login Failed |
| Invalid | Valid | Login Failed |
| Invalid | Invalid | Login Failed |

**4. State Transition Testing**

Checks how software behaves when it moves from one state to another.

Example:

A banking application may lock an account after a specified number of consecutive unsuccessful login attempts.

### Advantages

- No programming knowledge is required.
- Tests application functionality from the user's perspective.
- Helps identify missing or incorrect functionality.
- Suitable for manual testing.
- Can be based directly on requirements.

### Disadvantages

- Internal code defects may remain undiscovered.
- Test coverage depends on available requirements and test design.
- Some hidden logic problems may not be identified.
- It may be difficult to identify the exact cause of a defect.

### Common Tools

- Selenium.
- Postman.
- Jira.
- Zephyr.
- Browser Developer Tools.

---

## White Box vs Black Box Testing

| Basis | White Box Testing | Black Box Testing |
|---|---|---|
| Meaning | Tests internal code and structure. | Tests external functionality. |
| Knowledge Required | Programming knowledge. | Requirement and functional knowledge. |
| Focus | Internal logic. | Input and output behavior. |
| Performed By | Primarily Developers. | Testers and QA Engineers. |
| Source Code | Examined. | Not required. |
| Techniques | Statement, Branch, Condition, Path Coverage. | Equivalence Partitioning, BVA, Decision Tables. |
| Example | Testing code conditions. | Testing login functionality. |

### Easy Way to Remember

```text
White Box = Inside the Software
Black Box = Outside the Software
```

---

# 6. Static Testing

## Definition

**Static Testing is a testing technique in which software work products are examined without executing the application.**

It helps identify defects in requirements, design documents, source code, and other development documents.

### Objectives

- Identify defects early.
- Improve requirement quality.
- Detect missing information.
- Improve code quality.
- Reduce development costs.
- Prevent defects before execution.

### Static Testing Activities

**1. Reviews**

A review is an examination of software work products to identify problems and suggest improvements.

Types of reviews:

- Informal Review.
- Walkthrough.
- Technical Review.
- Inspection.

**2. Static Code Analysis**

Tools examine source code without executing it to identify possible issues.

Examples:
- SonarQube.
- ESLint.
- Checkstyle.

**3. Document Reviews**

Testers and other team members review:
- Requirement documents.
- Design documents.
- Test plans.
- Test cases.
- User manuals.

### Example

Suppose a requirement document states:

"The password must contain at least eight characters."

During a review, the tester discovers that another section states:

"The password must contain at least six characters."

This inconsistency is identified without executing the application.

This is Static Testing.

### Advantages

- Finds defects early.
- Reduces the cost of fixing defects.
- Does not require a running application.
- Improves documentation.
- Helps prevent defects.

### Disadvantages

- Cannot identify all runtime defects.
- Requires proper review knowledge.
- Some tools may produce false positives.
- Complex reviews can take time.

---

# 7. Dynamic Testing

## Definition

**Dynamic Testing is a testing technique in which software is executed with different inputs to verify its actual behavior against expected results.**

In simple words, Dynamic Testing means running the application and checking whether it works correctly.

### Objectives

- Verify application functionality.
- Identify runtime defects.
- Check actual outputs.
- Validate user interactions.
- Evaluate application performance.
- Identify unexpected behavior.

### Dynamic Testing Activities

1. Executing test cases.
2. Entering test data.
3. Checking actual results.
4. Comparing actual and expected results.
5. Reporting defects.
6. Retesting fixed defects.

### Example

Consider a registration page.

The tester:
- Enters a valid name.
- Enters a valid email.
- Enters a password.
- Clicks the Register button.

Expected Result:

The account should be created successfully.

Actual Result:

The application displays "Registration Successful."

The tester is executing the application and checking its behavior.

This is Dynamic Testing.

### Types of Dynamic Testing

Dynamic Testing includes many testing techniques and levels, such as:

- Unit Testing.
- Integration Testing.
- System Testing.
- Acceptance Testing.
- Functional Testing.
- Non-Functional Testing.
- Regression Testing.

### Advantages

- Identifies runtime defects.
- Verifies actual application behavior.
- Checks functionality with real inputs.
- Helps identify performance problems.
- Validates user workflows.

### Disadvantages

- Requires an executable application or component.
- Test execution can be time-consuming.
- Complete input coverage is generally impossible.
- Some defects may remain undiscovered.

---

## Static Testing vs Dynamic Testing

| Basis | Static Testing | Dynamic Testing |
|---|---|---|
| Meaning | Examines work products without execution. | Tests software through execution. |
| Execution | Not required. | Required. |
| Focus | Documents, design, and code. | Application behavior. |
| Objective | Prevent defects early. | Identify defects during execution. |
| Activities | Reviews, inspections, static analysis. | Test case execution, functional testing. |
| Example | Reviewing login requirements. | Executing login test cases. |
| Stage | Can begin early in development. | Requires an executable component or application. |

### Easy Way to Remember

```text
Static Testing  = Without Execution
Dynamic Testing = With Execution
```

---

# 8. Important Comparison: Testing Concepts

| Concept | Main Focus | Simple Explanation |
|---|---|---|
| QA | Process | Prevent defects. |
| QC | Product | Detect defects. |
| QE | Engineering | Build quality into development. |
| Verification | Specifications | Are we building the product right? |
| Validation | User needs | Are we building the right product? |
| White Box | Internal code | Check how software works internally. |
| Black Box | External functionality | Check what software does. |
| Static Testing | No execution | Review documents and code. |
| Dynamic Testing | Execution | Run software and check results. |

---

# 9. Important Interview Questions and Answers

## Basic Questions

**Q1. What is QA?**

Quality Assurance is a process-oriented approach that focuses on preventing defects by improving development processes.

**Q2. What is QC?**

Quality Control is a product-oriented approach that focuses on identifying defects in the software.

**Q3. What is QE?**

Quality Engineering uses engineering practices, automation, and continuous testing to build quality throughout software development.

**Q4. What is Verification?**

Verification checks whether software work products meet specified requirements and design specifications.

**Q5. What is Validation?**

Validation checks whether software meets user needs and intended requirements.

**Q6. What are the four levels of software testing?**

Unit Testing, Integration Testing, System Testing, and Acceptance Testing.

**Q7. What is White Box Testing?**

White Box Testing examines the internal code, structure, and logic of software.

**Q8. What is Black Box Testing?**

Black Box Testing checks software functionality without examining its internal source code.

**Q9. What is Static Testing?**

Static Testing examines software work products without executing the application.

**Q10. What is Dynamic Testing?**

Dynamic Testing executes software with different inputs to verify its actual behavior.

## Intermediate Questions

**Q11. What is the difference between QA and QC?**

QA focuses on improving processes to prevent defects, whereas QC focuses on examining the product to identify defects.

**Q12. Can testing be performed without executing software?**

Yes. Static Testing includes reviews, inspections, walkthroughs, and static code analysis.

**Q13. Which testing technique requires programming knowledge?**

White Box Testing generally requires programming and code understanding.

**Q14. Which testing technique is commonly used in Manual Testing?**

Black Box Testing is commonly used in Manual Testing because testers verify application behavior against requirements without needing to inspect source code.

**Q15. What is Boundary Value Analysis?**

Boundary Value Analysis is a Black Box Testing technique that checks values at and around the boundaries of an input range.

**Q16. What is Equivalence Partitioning?**

It divides input data into groups expected to behave similarly, allowing testers to select representative test values.

**Q17. Who performs System Testing?**

System Testing is primarily performed by the testing or QA team.

**Q18. What is the difference between Unit Testing and Integration Testing?**

Unit Testing checks individual components, whereas Integration Testing checks whether multiple components work correctly together.

**Q19. Is White Box Testing always performed by developers?**

No. Developers commonly perform it, but automation engineers and technical test engineers can also perform White Box Testing.

**Q20. Can Static and Dynamic Testing be performed together?**

Yes. Both approaches complement each other and help improve overall software quality.

---

# 10. Practical Assignments

Complete these exercises to strengthen your understanding.

## Assignment 1: QA vs QC vs QE

Consider an e-commerce application.

Identify whether the following activities belong to QA, QC, or QE:

1. Reviewing development processes.
2. Executing login test cases.
3. Automating regression tests.
4. Preparing quality standards.
5. Reporting a payment defect.
6. Integrating automated tests into a CI/CD pipeline.

## Assignment 2: Verification vs Validation

Classify these activities:

1. Reviewing an SRS document.
2. Reviewing UI design.
3. Executing registration test cases.
4. Checking whether payment works correctly.
5. Reviewing source code.

## Assignment 3: Testing Levels

Consider a food delivery application.

Give one practical example each for:

- Unit Testing.
- Integration Testing.
- System Testing.
- Acceptance Testing.

## Assignment 4: White Box vs Black Box

Consider the following code:

```javascript
function calculateDiscount(amount) {

    if (amount >= 1000) {
        return amount * 0.10;
    }

    return 0;
}
```

Answer:

1. What is the purpose of this function?
2. What input would execute the IF condition?
3. What input would execute the other path?
4. How would a White Box Tester test this function?
5. How would a Black Box Tester test the same functionality?

## Assignment 5: Static vs Dynamic Testing

Identify whether these activities are Static or Dynamic Testing:

1. Reviewing a requirement document.
2. Executing a login test case.
3. Performing a code review.
4. Testing a payment transaction.
5. Performing static code analysis.
6. Checking application behavior after submitting a form.

## Assignment 6: Think Like a Tester

Consider a banking application.

Identify:
- Five QA activities.
- Five QC activities.
- Three possible QE activities.
- Two Static Testing activities.
- Five Dynamic Testing scenarios.

---

# 11. Chapter Summary

| Topic | Key Learning |
|---|---|
| QA | Process-oriented defect prevention. |
| QC | Product-oriented defect detection. |
| QE | Engineering-driven quality improvement. |
| Verification | Checks work products against specifications. |
| Validation | Checks whether software meets user needs. |
| Unit Testing | Tests individual components. |
| Integration Testing | Tests interactions between modules. |
| System Testing | Tests the complete application. |
| Acceptance Testing | Checks business acceptance. |
| White Box Testing | Tests internal code and logic. |
| Black Box Testing | Tests external functionality. |
| Static Testing | Testing without executing software. |
| Dynamic Testing | Testing through software execution. |

---

# ✅ Chapter Completion Checklist

- [ ] Understand QA.
- [ ] Understand QC.
- [ ] Understand QE.
- [ ] Differentiate QA, QC, and QE.
- [ ] Understand Verification and Validation.
- [ ] Differentiate Verification and Validation.
- [ ] Understand all four testing levels.
- [ ] Understand White Box Testing.
- [ ] Understand Black Box Testing.
- [ ] Learn White Box Testing techniques.
- [ ] Learn Black Box Testing techniques.
- [ ] Understand Static Testing.
- [ ] Understand Dynamic Testing.
- [ ] Practice interview questions.
- [ ] Complete practical assignments.

---

**Previous Topic:** SDLC, STLC and Software Development Models.

**Next Topic:** System Testing Types.

**Learning Philosophy:** Understand the concept → Compare related concepts → Explore real-world examples → Practice → Prepare for interviews.