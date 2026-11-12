# 📘 SDLC, STLC and Software Development Models

This chapter explains how software is developed and tested throughout its life cycle. It covers SDLC, STLC, and three important software development models: Waterfall, Spiral, and V-Model.

Understanding these concepts is important for Manual Software Testers because testers need to know when testing starts, how testing activities are performed, and how software development models affect the testing process.

---

# 1. SDLC (Software Development Life Cycle)

## Definition

**SDLC stands for Software Development Life Cycle.**

It is a systematic process used by software development teams to plan, design, develop, test, deploy, and maintain software applications.

In simple words, SDLC describes the complete journey of software development, from the initial idea to the final product and its maintenance.

### Why Do We Need SDLC?

SDLC provides a structured approach to software development.

Its main objectives are:

1. Develop high-quality software.
2. Complete projects within the planned timeline.
3. Manage development costs.
4. Understand customer requirements.
5. Reduce development risks.
6. Improve communication between team members.
7. Deliver software that meets business requirements.

## Phases of SDLC

SDLC generally consists of the following phases:

### Phase 1: Requirement Gathering and Analysis

In this phase, the development team collects and understands the requirements of the customer.

The team identifies:
- What the customer wants.
- What features are required.
- Who will use the application.
- What problems the software should solve.
- Technical and business requirements.

**Example:**

A customer wants an online shopping application.

Requirements may include:
- User registration.
- User login.
- Product search.
- Add to cart.
- Online payment.
- Order tracking.

**People Involved:**
- Business Analyst (BA).
- Project Manager.
- Customer or Client.
- Stakeholders.

**Document Prepared:**
- BRD (Business Requirement Document).
- SRS (Software Requirement Specification).
- FRS (Functional Requirement Specification).

### Phase 2: Feasibility Study

In this phase, the team evaluates whether the proposed software project is practical and achievable.

The team checks:

1. Technical Feasibility – Can the software be developed using available technology?
2. Economic Feasibility – Is the project financially affordable?
3. Operational Feasibility – Will the software work effectively in the organization?
4. Legal Feasibility – Does the project comply with applicable laws and regulations?
5. Schedule Feasibility – Can the project be completed within the available time?

**Example:**

Before developing a payment application, the company checks whether it has the technology, budget, and resources to build and maintain it.

### Phase 3: Design

In this phase, the development team creates the architecture and design of the software.

It describes how the software will look and how different components will work together.

Two important design levels are:

**1. High-Level Design (HLD)**

Describes the overall architecture of the application.

It includes:
- System architecture.
- Major modules.
- Database architecture.
- Technology selection.
- Communication between components.

**2. Low-Level Design (LLD)**

Describes the internal details of individual modules.

It includes:
- Detailed logic.
- Algorithms.
- Class diagrams.
- Function descriptions.
- Database tables and relationships.

**Example:**

For an online shopping application:

HLD:
- Login module.
- Product module.
- Cart module.
- Payment module.

LLD:
- Login validation logic.
- Password encryption logic.
- Cart calculation logic.
- Payment processing logic.

**People Involved:**
- Software Architects.
- UI/UX Designers.
- Technical Leads.
- Developers.

### Phase 4: Development (Coding)

In this phase, developers convert the approved design into actual software using programming languages.

Examples:
- Java.
- Python.
- C++.
- JavaScript.
- PHP.

Development activities include:
- Writing source code.
- Creating database connections.
- Developing application modules.
- Implementing business logic.
- Performing code reviews.

**Example:**

Developers create the registration, login, product search, and payment functionality of an e-commerce application.

### Phase 5: Testing

In this phase, testers evaluate the developed software to identify defects and verify whether it meets the specified requirements.

Testing activities include:
- Understanding requirements.
- Preparing test scenarios.
- Writing test cases.
- Preparing test data.
- Executing test cases.
- Reporting defects.
- Retesting fixed defects.
- Performing regression testing.

**Example:**

For an online shopping application, testers verify:
- Whether users can register.
- Whether login works correctly.
- Whether products are displayed correctly.
- Whether cart calculations are accurate.
- Whether payments are processed correctly.

**People Involved:**
- Manual Testers.
- Automation Testers.
- QA Engineers.
- Developers.

### Phase 6: Deployment

In this phase, the tested and approved software is released into the production environment for actual users.

Deployment activities include:
- Installing the application.
- Configuring production servers.
- Setting up databases.
- Releasing software.
- Making the application available to users.

**Example:**

The company launches its shopping application on the internet so customers can purchase products.

### Phase 7: Maintenance

After deployment, the software requires continuous monitoring, support, and improvement.

Maintenance activities include:
- Fixing bugs.
- Improving performance.
- Adding new features.
- Updating security.
- Supporting users.
- Maintaining compatibility.

**Example:**

After launching the shopping application, the company releases an update to fix a payment issue reported by customers.

## SDLC Diagram

```text
   Requirement Gathering
            |
            ↓
      Feasibility Study
            |
            ↓
           Design
            |
            ↓
        Development
            |
            ↓
          Testing
            |
            ↓
         Deployment
            |
            ↓
        Maintenance
            |
            ↓
           End
```

**Note:** This is a simplified sequential representation. The actual sequence and overlap of activities depend on the development methodology being used.

## Advantages of SDLC

- Provides a structured development process.
- Improves project planning.
- Helps manage resources.
- Improves software quality.
- Reduces development risks.
- Makes project tracking easier.

## Disadvantages of SDLC

- Some models require extensive documentation.
- Changes can be difficult in sequential approaches.
- Development may take considerable time.
- Poor requirement analysis can affect the entire project.

---

# 2. STLC (Software Testing Life Cycle)

## Definition

**STLC stands for Software Testing Life Cycle.**

It is a systematic process followed by the testing team to perform software testing activities.

In simple words, STLC explains how testers plan, prepare, execute, and complete the testing process.

STLC focuses specifically on software testing activities within the overall software development process.

### Objectives of STLC

1. Identify defects in software.
2. Verify that requirements are satisfied.
3. Prepare effective test cases.
4. Ensure proper test execution.
5. Track and report defects.
6. Improve software quality.
7. Complete testing within the planned timeline.

## Phases of STLC

### Phase 1: Requirement Analysis

In this phase, testers analyze the requirements to understand what needs to be tested.

Testers identify:
- Functional requirements.
- Non-functional requirements.
- Testable requirements.
- Testing scope.
- Required test data.
- Possible risks.

**Example:**

For a login page, testers identify requirements such as:
- Login using valid credentials.
- Reject invalid credentials.
- Display validation messages.
- Handle empty fields.

**Tester Activities:**
- Read SRS and FRS documents.
- Understand business requirements.
- Identify test scenarios.
- Clarify doubts with Business Analysts.
- Identify automation possibilities.

**Deliverables:**
- Requirement Understanding Document.
- Requirement Traceability Matrix (RTM), when prepared at this stage.
- List of testing requirements.

### Phase 2: Test Planning

In this phase, the test manager or test lead prepares the test plan.

The test plan explains how testing will be performed.

It includes:
- Testing scope.
- Testing objectives.
- Testing strategy.
- Required resources.
- Roles and responsibilities.
- Testing schedule.
- Testing tools.
- Entry and exit criteria.
- Risks and mitigation plans.

**Example:**

For an online shopping application:

- Testing duration: 15 days.
- Testing type: Functional and Regression Testing.
- Testing tool: Jira.
- Test environment: Chrome and Firefox.
- Team: 3 Manual Testers.

**Deliverable:**
- Test Plan Document.

### Phase 3: Test Case Development

In this phase, testers create detailed test cases based on the requirements.

A test case generally contains:

1. Test Case ID.
2. Test Scenario.
3. Preconditions.
4. Test Steps.
5. Test Data.
6. Expected Result.
7. Actual Result.
8. Status (Pass/Fail).

**Example: Login Test Case**

| Field | Details |
|---|---|
| Test Case ID | TC_LOGIN_001 |
| Scenario | Verify login with valid credentials. |
| Preconditions | User must have a registered account. |
| Test Steps | Enter valid username and password and click Login. |
| Test Data | Valid username and password. |
| Expected Result | User should log in successfully. |
| Actual Result | To be recorded during execution. |
| Status | Not Executed |

Testers may also prepare:
- Test data.
- Test scripts.
- RTM updates.
- Test cases for positive and negative scenarios.

**Deliverables:**
- Test Cases.
- Test Data.
- Updated RTM.

### Phase 4: Test Environment Setup

In this phase, the testing team prepares the environment required to execute test cases.

A test environment generally includes:
- Hardware.
- Software.
- Operating system.
- Browser.
- Database.
- Network configuration.
- Test application.
- Required testing tools.

**Example:**

For testing a web application, the team may configure:

- Windows 11.
- Google Chrome.
- Firefox.
- MySQL Database.
- Test Server.

**Environment Smoke Testing:**

After environment setup, testers perform basic checks to verify whether the application is ready for testing.

**Deliverables:**
- Configured Test Environment.
- Environment Readiness Report.

### Phase 5: Test Execution

In this phase, testers execute the prepared test cases against the application.

Testers compare the actual result with the expected result.

There are generally two outcomes:

**Pass:** Actual result matches expected result.

**Fail:** Actual result does not match expected result.

**Example:**

Expected Result: Clicking Login with valid credentials should open the dashboard.

Actual Result: Application displays an error message.

Status: FAIL.

Tester activities:
- Execute test cases.
- Record actual results.
- Mark test cases Pass or Fail.
- Identify defects.
- Report defects.
- Perform retesting after fixes.
- Perform regression testing when required.

**Deliverables:**
- Test Execution Report.
- Defect Reports.
- Updated Test Cases.

### Phase 6: Defect Reporting and Tracking

When testers identify a defect, they report it to the development team using a defect tracking tool.

Common tools:
- Jira.
- Bugzilla.
- Azure DevOps.

A defect report generally includes:

- Bug ID.
- Bug Title.
- Description.
- Steps to Reproduce.
- Expected Result.
- Actual Result.
- Severity.
- Priority.
- Environment.
- Screenshots or Attachments.

**Example:**

Bug Title: Login button does not respond after entering valid credentials.

Expected Result: User should successfully log in.

Actual Result: Nothing happens after clicking the Login button.

Severity: Major (depending on the impact).

Priority: High (depending on business urgency).

### Phase 7: Test Closure

This is the final phase of STLC.

In this phase, the testing team evaluates the completed testing activities and prepares the final testing summary.

Activities include:
- Checking test execution completion.
- Reviewing passed and failed test cases.
- Reviewing unresolved defects.
- Preparing test summary reports.
- Checking exit criteria.
- Documenting lessons learned.

**Deliverables:**
- Test Closure Report.
- Test Summary Report.
- Defect Summary.
- Lessons Learned Document.

## STLC Diagram

```text
      Requirement Analysis
              |
              ↓
         Test Planning
              |
              ↓
      Test Case Development
              |
              ↓
     Test Environment Setup
              |
              ↓
         Test Execution
              |
              ↓
    Defect Reporting & Tracking
              |
              ↓
         Test Closure
              |
              ↓
             End
```

**Note:** Defect reporting and tracking generally happen throughout test execution rather than only as a separate final activity.

## Advantages of STLC

- Provides a structured testing process.
- Improves test coverage.
- Helps identify defects systematically.
- Improves communication.
- Makes testing activities easier to track.
- Helps deliver reliable software.

---

# 3. SDLC vs STLC

SDLC and STLC are closely related but serve different purposes.

| Basis | SDLC | STLC |
|---|---|---|
| Full Form | Software Development Life Cycle | Software Testing Life Cycle |
| Main Focus | Software development. | Software testing. |
| Objective | Develop software. | Verify and validate software. |
| Activities | Requirement, design, coding, testing, deployment, maintenance. | Requirement analysis, test planning, test design, execution, closure. |
| Participants | Developers, BA, designers, testers, managers. | Testers, QA engineers, test leads, developers. |
| Output | Working software. | Testing results and quality information. |
| Scope | Entire software development process. | Testing activities within the development process. |

### Relationship Between SDLC and STLC

```text
              SDLC
                |
    -------------------------
    |           |           |
 Requirements  Design    Development
                            |
                            ↓
                       Testing
                            |
                            ↓
                           STLC
                            |
                   Testing Activities
                            |
                            ↓
                       Test Closure
```

**Important:** STLC is part of the broader SDLC process. Testing is not necessarily performed only after development; depending on the methodology, testing activities can begin during requirement analysis and design.

---

# 4. Waterfall Model

## Definition

The Waterfall Model is a traditional software development model in which development activities are performed sequentially, one phase after another.

A new phase generally starts after the previous phase is completed and approved.

It is called the Waterfall Model because the process flows downward like a waterfall.

## Phases of Waterfall Model

1. Requirement Analysis.
2. System Design.
3. Implementation (Coding).
4. Testing.
5. Deployment.
6. Maintenance.

## Waterfall Model Diagram

```text
    Requirement Analysis
             |
             ↓
        System Design
             |
             ↓
       Implementation
             |
             ↓
           Testing
             |
             ↓
         Deployment
             |
             ↓
         Maintenance
```

## Real-World Example

Suppose a company wants to develop a simple employee management system.

The company follows the Waterfall Model.

**Step 1: Requirement Analysis**

The company collects requirements such as:
- Employee registration.
- Employee login.
- Attendance management.
- Salary management.

**Step 2: Design**

The development team prepares the database design and application architecture.

**Step 3: Development**

Developers implement all the required features.

**Step 4: Testing**

Testers verify the application after development is completed.

**Step 5: Deployment**

The application is released for employees.

**Step 6: Maintenance**

The company fixes bugs and provides updates.

## Role of a Tester in the Waterfall Model

In the traditional Waterfall approach, major testing activities take place after the development phase.

Tester responsibilities include:
- Understanding requirements.
- Reviewing requirement documents.
- Preparing test cases.
- Preparing test data.
- Executing test cases.
- Reporting defects.
- Retesting fixed defects.
- Performing regression testing.

Although formal testing may occur later, testers can participate in requirement reviews earlier.

## Advantages of Waterfall Model

1. Simple and easy to understand.
2. Clearly defined development phases.
3. Easy to manage.
4. Suitable for projects with stable requirements.
5. Documentation is maintained throughout the process.

## Disadvantages of Waterfall Model

1. Difficult to accommodate requirement changes.
2. Testing generally happens later.
3. Defects discovered late can be expensive to fix.
4. Working software is not available until later stages.
5. Not ideal for projects with frequently changing requirements.

## When to Use Waterfall Model?

- Requirements are clearly defined.
- Requirements are unlikely to change.
- Project scope is fixed.
- Technology is well understood.
- Documentation and approvals are important.

---

# 5. Spiral Model

## Definition

The Spiral Model is a risk-driven software development model that combines iterative development with systematic risk analysis.

In this model, software is developed through multiple cycles called spirals.

Each cycle involves planning, risk analysis, development, and evaluation.

The main focus of the Spiral Model is identifying and managing risks throughout software development.

## Four Main Activities of the Spiral Model

### 1. Planning

The team identifies:
- Project objectives.
- Requirements.
- Available resources.
- Cost.
- Time.
- Constraints.

**Example:** Decide which features should be developed in the next cycle.

### 2. Risk Analysis

The team identifies possible risks and evaluates their impact.

Examples:
- Security risks.
- Technical risks.
- Budget risks.
- Performance risks.
- Integration risks.

The team may develop a prototype to understand and reduce major risks.

### 3. Engineering (Development and Testing)

The team develops and tests the selected functionality.

Activities include:
- Designing.
- Coding.
- Testing.
- Integrating modules.

### 4. Evaluation

The customer or stakeholder reviews the developed version and provides feedback.

The team uses this feedback to plan the next spiral.

## Spiral Model Diagram

```text
       ┌──────────────────────┐
       │       Planning       │
       └──────────┬───────────┘
                  ↓
       ┌──────────────────────┐
       │     Risk Analysis    │
       └──────────┬───────────┘
                  ↓
       ┌──────────────────────┐
       │ Development & Testing│
       └──────────┬───────────┘
                  ↓
       ┌──────────────────────┐
       │      Evaluation      │
       └──────────┬───────────┘
                  |
                  ↓
          Next Spiral Cycle
                  |
                  ↺
```

*Conceptual representation: The actual Spiral Model is represented as expanding loops around a central point.*

## Real-World Example

Suppose a company wants to develop a large online banking application.

Since banking software involves financial transactions and sensitive customer information, the project has significant risks.

The company uses the Spiral Model.

**First Spiral:**

- Plan basic banking requirements.
- Identify security risks.
- Develop a login prototype.
- Evaluate the prototype.

**Second Spiral:**

- Plan account management.
- Analyze data security risks.
- Develop account management.
- Test account functionality.
- Collect feedback.

**Third Spiral:**

- Plan money transfer functionality.
- Analyze transaction risks.
- Develop payment functionality.
- Test transactions.
- Evaluate results.

The process continues until the required application is developed.

## Role of a Tester in the Spiral Model

Testing is performed during every development cycle.

Tester responsibilities include:
- Reviewing requirements.
- Identifying potential risks.
- Testing prototypes.
- Testing developed features.
- Reporting defects.
- Performing regression testing.
- Validating customer feedback.

## Advantages of Spiral Model

1. Strong focus on risk management.
2. Supports changing requirements.
3. Customer feedback is collected regularly.
4. Testing occurs in every cycle.
5. Suitable for large and complex projects.

## Disadvantages of Spiral Model

1. Expensive to implement.
2. Requires experienced professionals.
3. Risk analysis can be complex.
4. Project management is difficult.
5. Not suitable for small projects with limited budgets.

## When to Use Spiral Model?

- Large projects.
- Complex applications.
- High-risk projects.
- Projects with changing requirements.
- Projects requiring continuous customer feedback.

---

# 6. V-Model (Verification and Validation Model)

## Definition

The V-Model stands for Verification and Validation Model.

It is a software development model in which each development phase has a corresponding testing phase.

It is also called the Verification and Validation Model because development activities are associated with verification, while corresponding testing activities are associated with validation.

The model is represented in the shape of the letter V.

## Understanding Verification and Validation

### Verification

Verification checks whether the software is being developed correctly according to specifications and design documents.

**Question:** Are we building the product right?

Examples:
- Requirement reviews.
- Design reviews.
- Code reviews.
- Document inspections.

Verification activities generally do not require executing the software.

### Validation

Validation checks whether the developed software meets user needs and intended requirements.

**Question:** Are we building the right product?

Examples:
- Unit Testing.
- Integration Testing.
- System Testing.
- Acceptance Testing.

Validation generally involves executing the software.

## Phases of V-Model

The left side represents development and verification activities.

The right side represents corresponding testing and validation activities.

### Left Side: Verification Activities

**1. Requirement Analysis**

The team collects and analyzes customer requirements.

Corresponding Testing Phase: Acceptance Testing.

**2. System Design**

The overall system architecture and system requirements are defined.

Corresponding Testing Phase: System Testing.

**3. High-Level Design (HLD)**

The system is divided into modules and their interactions are designed.

Corresponding Testing Phase: Integration Testing.

**4. Low-Level Design (LLD)**

Detailed internal module logic is designed.

Corresponding Testing Phase: Unit Testing.

**5. Coding**

Developers implement the software based on the approved design.

### Right Side: Validation Activities

**1. Unit Testing**

Individual components or units are tested independently.

Example: Testing a function that calculates the total price.

**2. Integration Testing**

Multiple modules are combined and tested to check whether they work together correctly.

Example: Checking communication between the shopping cart and payment module.

**3. System Testing**

The complete application is tested against the specified system requirements.

Example: Testing the complete online shopping application.

**4. Acceptance Testing**

The application is checked to determine whether it meets business requirements and is ready for acceptance.

Example: Customers verify that the shopping application supports all required purchasing operations.

## V-Model Diagram

```text
       VERIFICATION              VALIDATION

    Requirement Analysis  -------- Acceptance Testing
             \                         /
              \                       /
               \                     /
             System Design  -------- System Testing
                 \                   /
                  \                 /
                   \               /
               High-Level Design -- Integration Testing
                      \           /
                       \         /
                        \       /
               Low-Level Design - Unit Testing
                         \     /
                          \   /
                           \ /
                          Coding
```

### Relationship Between Development and Testing Phases

| Development Phase | Corresponding Testing Phase |
|---|---|
| Requirement Analysis | Acceptance Testing |
| System Design | System Testing |
| High-Level Design | Integration Testing |
| Low-Level Design | Unit Testing |
| Coding | Implementation of software |

**Important:** Test planning and test design can begin early, alongside the corresponding development phases.

## Real-World Example

Suppose a company develops an online banking application using the V-Model.

| Development Activity | Corresponding Testing Activity |
|---|---|
| Collect banking requirements. | Acceptance Testing |
| Design the complete banking system. | System Testing |
| Design interactions between account and payment modules. | Integration Testing |
| Design internal transaction functions. | Unit Testing |
| Write the application code. | Execute planned testing at the appropriate stages. |

## Role of a Tester in V-Model

Testers are involved early in the development process.

Their responsibilities include:
- Reviewing requirements.
- Identifying test conditions.
- Preparing acceptance test scenarios.
- Preparing system test cases.
- Preparing integration test cases.
- Preparing unit test cases or supporting developers with test requirements.
- Executing the corresponding tests.
- Reporting defects.
- Retesting and regression testing.

## Advantages of V-Model

1. Testing is planned from the beginning.
2. Every development phase has a corresponding testing phase.
3. Defects can be identified earlier through reviews and testing preparation.
4. Requirements and test activities remain closely connected.
5. Simple and easy to understand.
6. Suitable for projects with clearly defined requirements.

## Disadvantages of V-Model

1. Difficult to accommodate changing requirements.
2. Less flexible than iterative models.
3. Working software is available relatively late.
4. Not ideal for complex projects with frequently changing requirements.
5. Changes to requirements may require significant rework.

## When to Use V-Model?

- Requirements are clear and stable.
- Project scope is well defined.
- Testing and documentation are important.
- Development requires a structured process.
- The project has strict quality requirements.

---

# 7. Comparison of Waterfall, Spiral and V-Model

| Basis | Waterfall | Spiral | V-Model |
|---|---|---|---|
| Approach | Sequential | Iterative and risk-driven | Sequential with corresponding testing phases |
| Main Focus | Completing phases in order | Risk identification and management | Verification and validation |
| Testing | Major testing phase after development | Every cycle | Planned alongside development |
| Risk Management | Limited explicit risk analysis | Strong risk management | Generally less risk-focused than Spiral |
| Flexibility | Low | High | Low |
| Customer Feedback | Usually at defined milestones | After each cycle | Usually at defined milestones |
| Cost | Depends on project | Generally high | Depends on project |
| Best For | Stable requirements | Large and high-risk projects | Stable requirements with structured testing |

## Quick Revision

**Waterfall Model:** Complete one phase before moving to the next.

**Spiral Model:** Develop software through repeated cycles with risk analysis.

**V-Model:** Every development phase has a corresponding testing phase.

---

# 8. Important Interview Questions and Answers

### Q1. What is SDLC?

SDLC stands for Software Development Life Cycle. It is a structured process used to develop software through phases such as requirement gathering, design, development, testing, deployment, and maintenance.

### Q2. What are the phases of SDLC?

The common phases are:

1. Requirement Gathering and Analysis.
2. Feasibility Study.
3. Design.
4. Development.
5. Testing.
6. Deployment.
7. Maintenance.

### Q3. What is STLC?

STLC stands for Software Testing Life Cycle. It is a systematic process followed by testers to analyze requirements, plan testing, design test cases, prepare the environment, execute tests, report defects, and close testing activities.

### Q4. What are the phases of STLC?

1. Requirement Analysis.
2. Test Planning.
3. Test Case Development.
4. Test Environment Setup.
5. Test Execution.
6. Defect Reporting and Tracking.
7. Test Closure.

### Q5. What is the difference between SDLC and STLC?

SDLC focuses on the complete software development process, whereas STLC focuses specifically on software testing activities.

### Q6. What is the Waterfall Model?

The Waterfall Model is a sequential software development model in which one phase is generally completed before the next phase begins.

### Q7. What is the Spiral Model?

The Spiral Model is a risk-driven development model in which software is developed through repeated cycles involving planning, risk analysis, engineering, and evaluation.

### Q8. What is the V-Model?

The V-Model is a software development model in which each development phase has a corresponding testing phase. It emphasizes verification and validation.

### Q9. Which model is best for changing requirements?

The Spiral Model is generally more suitable than Waterfall and V-Model when requirements change frequently, particularly for large and risk-intensive projects.

### Q10. What is Verification?

Verification checks whether software development activities and work products meet specified requirements and design specifications.

### Q11. What is Validation?

Validation checks whether the developed software satisfies user needs and intended requirements.

### Q12. What is the difference between Verification and Validation?

Verification asks, "Are we building the product right?"

Validation asks, "Are we building the right product?"

### Q13. When does testing start in the V-Model?

Testing activities are planned from the beginning. Test design and reviews start alongside development activities, while execution of different testing levels happens at their corresponding stages.

### Q14. Which model focuses on risk analysis?

The Spiral Model focuses strongly on risk identification, evaluation, and management.

### Q15. Can testers participate in requirement analysis?

Yes. Testers review requirements to identify ambiguities, missing information, inconsistencies, and testable conditions.

---

# 9. Practical Learning Tasks

Complete these activities to understand the concepts practically.

### Task 1: SDLC Understanding

Consider a company developing an online food delivery application.

Identify activities performed in each SDLC phase:

- Requirement Gathering.
- Feasibility Study.
- Design.
- Development.
- Testing.
- Deployment.
- Maintenance.

### Task 2: STLC Practice

Imagine you are testing a login page.

Write down the activities you would perform during each STLC phase.

### Task 3: Model Identification

Identify the appropriate development model for each situation:

1. A project has fixed and clearly defined requirements.
2. A large banking application has significant security and financial risks.
3. A project requires development phases to be closely matched with testing phases.

### Task 4: Verification vs Validation

Classify the following activities:

1. Reviewing requirement documents.
2. Reviewing application architecture.
3. Executing login test cases.
4. Checking whether a payment is processed correctly.
5. Reviewing source code.

### Task 5: Interview Preparation

Explain the following topics without reading your notes:

- SDLC.
- STLC.
- Difference between SDLC and STLC.
- Waterfall Model.
- Spiral Model.
- V-Model.
- Verification vs Validation.

---

# 10. Chapter Summary

| Topic | Key Learning |
|---|---|
| SDLC | Complete software development life cycle. |
| STLC | Complete software testing life cycle. |
| Waterfall Model | Sequential development approach. |
| Spiral Model | Iterative and risk-driven development approach. |
| V-Model | Development phases mapped to testing phases. |
| Verification | Checking work products against specifications. |
| Validation | Checking whether software meets user needs. |

---

# ✅ Chapter Completion Checklist

- [ ] Understand SDLC.
- [ ] Learn all SDLC phases.
- [ ] Understand STLC.
- [ ] Learn all STLC phases.
- [ ] Understand the difference between SDLC and STLC.
- [ ] Understand the Waterfall Model.
- [ ] Understand the Spiral Model.
- [ ] Understand the V-Model.
- [ ] Learn Verification and Validation.
- [ ] Compare all three development models.
- [ ] Complete practical assignments.
- [ ] Prepare interview questions.

---

**Previous Topic:** Software Testing Fundamentals.

**Next Topic:** QA vs QC vs QE.

**Learning Philosophy:** Understand the process → Learn the phases → Compare the models → Practice real-world examples → Prepare for interviews.