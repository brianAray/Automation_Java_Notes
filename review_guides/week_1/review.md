# Week 1 - Test Mentality

## Testing Philosophy
---
### Testing Mindset
---
- **Developer Mindset**
    - Testing should be approached like writing code, with a focus on quality and defect prevention. 
    - Developers should take ownership of the quality of the software they produce and strive to prevent defects from occurring.
- **Test Mindset**
    - Having a mindset focused on testing and quality is essential for producing reliable software. 
    - Considering testing and quality throughout the entire software development life cycle, not just during testing phases.
### Why Test
---
- **Objectives of Testing**
    - The objective of software testing is to ensure that the software meets the desired quality and functionality. This includes:
        - Verifying that the software satisfies the specified requirements
        - Verify the software is reliable
        - Verify that it performs as expected
- **Quality Management**
    - Quality management involves the processes for ensuring that the software meets the required quality standards. It includes:
        - The Development of Quality Control Procedures
        - Test Planning
        - Test Execution.
- **Verification vs Validation**
    - Verification is concerned with ensuring that the software is built correctly and meets the specified requirements.
        - ```md
          > The requirement is that a login page should have two fields for username and password
          > Verification involves checking if the login page has two fields
    - Validation is concerned with ensuring that the right software is built and meets the needs of the user.
        - ```md
          > The user needs to be able to login to the system quickly and easily
          > Validation involves checking if the login page is intuitive, and the process is fast and efficient 
### Testing Principles
---
- **Test Reveals Defects not their absence**
    - Testing is a process of finding defects, not proving perfection. 
    - No matter **how** comprehensive the testing is, it is **impossible** to ensure that the software is entirely error-free.
- **Exhaustive Testing is impossible**
    - It is **impossible** to test the software exhaustively, covering every possible input and scenario. 
    - Testing should be done strategically, focusing on the most critical and high-risk areas of the software.
- **Test Early**
    - Testing should be done as early as possible in the software development life cycle. 
    - This helps to prevent defects from propagating and becoming more expensive to fix.
- **Defect Cluster**
    - Defects often cluster around a specific area of code or functionality. 
    - Identifying these clusters can help to prioritize testing efforts and allocate resources more effectively.
    - Example:
        - ```md
          > A software is designed to handle user registration and login. 
          > During testing, testers find that there are several defects related to the password reset functionality:

          - The password reset link is not being sent to the user's email address
          - The password reset link is not valid when the user clicks on it
          - The user's password is not being reset correctly
- **Pesticide Paradox**
    - The Pesticide Paradox refers to the fact that repeating the same tests only finds the same defects. 
    - To ensure that testing is effective, testing strategies should evolve and change over time.
- **Test Context**
    - The environment in which software is tested includes hardware and software configurations, as well as other external factors that can affect the software's performance and behavior.
- **Absence of error fallacy**
    - Passing a test does not mean that there are no defects in the software. 
    - It is possible that the testing did not cover all possible scenarios or that some defects were missed.

## Test Case Design
---
### Terminology
---
- **High Level Testcase**
    - Test case that covers broad functionality of the system
    - Example: 
        - ```md
          # Login Functionality 
          - This test case would cover the entire login process, from entering valid/invalid credentials to successful login/logout

          # Registration Functionality
          - This would cover the entire registration process, from entering user information, validating it, then successfully registering
- **Low Level Testcase**
    - Test case that covers specific functionality of the system
    - Example: 
        - ```md
          # Button click event
          - This test case would ensure that clicking on a button would perform the expected action or event

          # Input Validation
          - This test case would ensure that invalid inputs are detected and handled properly by the system
          - This could include testing for input field length limits, data type validation, and character restrictions
- **Test Basis**
    - The test basis is the set of requirements and specifications used as the basis for creating test cases.
    - These would include:
        - **Requirements specification**
            - Outlines the functionality and features that the software system is intended to have
        - **Design specification**
            - Outlines the technical design of and architecture of the software system
        - **User stories**
            - Used in agile to for describing the user requirements and validate their interactions in test cases
        - **Use cases**
            - Used to describe interactions between users and the software
        - **Functional requirements**
            - Describe the behavior and functionality of the software
        - **Non-functional requirements**
            - Describe the non-functional requirements like performance, usability, etc
        - **Existing software system**
            - If system already exists, use test cases to ensure the system continues to function as intended
- **Test Objective**
    - The test objective is the goal of a specific test case. It specifies what is being tested, how it is being tested, and what the expected outcome is.
- **Test Suite**
    - A test suite is a collection of test cases used to test a software system.
- **Test Data**
    - Data used in testing, including input data and expected output data
- **Test Object**
    - The test object is the software or system being tested.
- **Error/Defect/Failure**
    - An error is a mistake in the code, a defect is a problem in functionality, and a failure is when the software does not behave as expected.
    - **Error**
        - Developer accidentally types the wrong variable name in their code, system fails to compile
    - **Defect**
        - In an e-commerce website, the "Add to cart" button is not functioning correctly, and doesn't add the selected item to cart preventing user from purchasing
    - **Failure**
        - A user tries to book a hotel room, the software crashes during the booking process and the user cannot book a room
- **Use Case Stories**
    - Use case stories are a way of describing the functionality of a system from the user's perspective. 
    - They help to ensure that the software meets the needs of the user and that the user's requirements are translated into software specifications.
        - ```md
          "As a customer, I want to be able to add items to my shopping cart, so that I can purhcase them all at once"

          1. Test case: Add item to cart
            - Pre-condition: User is logged in and on product page
            - Steps: Click "Add to Cart" button
            - Expected result: Item is added to cart and cart count is updated
          
          2. Test case: Remove item from cart
            - Pre-condition: User has items in cart
            - Steps: Click "Remove" button next to item
            - Expected result: Item is removed from cart and cart count is updated
          
- **Requirements Traceability Matrix**
    - A Requirements Traceability Matrix (RTM) is a tool used to track requirements through the software development process.
    - It ensures that all requirements are met and that changes to requirements are properly tracked and managed.

### Technique
---
- **Equivalence Partitioning**
    - Equivalence partitioning is a testing technique that divides input values into equivalent groups to reduce the number of test cases required.
        - ```md
          > There is a login page of an application that requires a username and password
          
          The input values for the username and password can be divided into three equivalent groups:
          
          # Valid
            - Input values that are expected to be accepted by the system
            - Example: 
                - username: "john.doe"
                - password: "Password123"
          
          # Invalid
            - Input values that are expected to be rejected by the system
            - Example: 
                - username: "jo"
                - password: "pass"
                - These could be rejected based on not enough characters or missing types of characters like numbers

          # Boundary
            - Input values that are on the edge of the input range
            - Example: A boundary value for username could be a string that is exactly 20 characters long if the system accepts only between 5 - 20 characters 
- **Boundary Value Analysis**
    - Boundary Value Analysis is a testing technique that focuses on values at the boundary between valid and invalid input. 
    - It helps to identify defects that may arise from the software's handling of boundary values.
- **Decision Tables**
    - Decision Tables are a tool used to map out different conditions and actions of a software system.
    - They are useful for complex decision-making scenarios and help to ensure that all possible scenarios are covered in testing.
- **State Transition Diagrams**
    - State Transition Diagrams are a visual representation of the different states of a software system and how it transitions between them. 
    - They help to identify defects related to the system's behavior and transitions between different states.
- **Checklist Testing**
    - Checklist Testing is a testing technique that involves using a list of items to ensure that all necessary testing has been done. 
    - It helps to ensure that no critical areas are missed during testing.
- **Positive Testing**
    - Positive Testing is a testing technique that involves testing software with valid inputs to ensure that it behaves as expected. 
    - It helps to verify that the software functions correctly under normal operating conditions.
        - ```md
          > A website has a login page that requires a username and password

          Positive testing for this could include the following test cases:

            - Enter a valid username and password and get a successful verification
            - Enter a valid username and an incorrect password and verify the error message is displayed
            - Enter an incorrect username and password and verify the error message is displayed
- **Negative Testing**
    - Negative Testing is a testing technique that involves testing software with invalid inputs to ensure that it handles errors properly. 
    - It helps to identify defects related to error handling and exception handling.
        - ```md
          > A website has a login page that requires a username and password

          Negative testing for this could include the following test cases:

            - Enter a blank username and password and verify that the error message is displayed
            - Enter a valid username and a blank password and verify the error message is displayed
            - Enter a username longer than the allowed length and verify the error message is displayed
- **Experience Based Testing**
    - Testing based on experience, intuition, and knowledge gained through testing similar systems
    - Types:
        - Error guessing: testers predict and test for potential errors
        - Exploratory testing: testing approach that emphasizes learning, investigation, and experimentation to uncover defects
- **Risk Based Testing**
    - Testing that prioritizes tests based on risks associated with different parts of the software system
    - Process:
        - Identify potential risks associated with the software systems
        - Determine the likelihood and impact of each risk
        - Prioritize testing based on the level of risk associated with each area of the software system
- **Localisation Testing**
    - Testing approach that ensures software can be used effectively in different locales and languages
    - Process:
        - Test software with different locale and language settings to ensure that the software functions as expected
        - Test localized content (e.g. translated text) for accuracy, formatting, and readability
        - Test for any potential cultural or regional issues (e.g. date formats, currency symbols)
- **Accessibility Testing**
    - Testing approach that ensures software can be used effectively by users with disabilities
    - Process:
        - Test software with different accessibility settings (e.g. screen readers, voice recognition software) to ensure that the software functions as expected
        - Test for compliance with accessibility standards and guidelines (e.g. WCAG 2.1)
        - Test for any potential accessibility issues (e.g. color contrast, font size)
- **A-B Testing**
    - Testing approach that compares two versions of the software system to determine which performs better
    - Process:
        - Develop two versions of the software system (e.g. different user interfaces, pricing strategies, marketing campaigns)
        - Randomly assign users to each version and gather data on user behavior and performance metrics
        - Analyze data to determine which version performs better
- **Static Testing vs Dynamic Testing**
    - Static Testing examines code without executing it, while Dynamic Testing examines code as it's being executed.
    - The goal of static testing is to find defects early in the development process before the code is executed
    - It has several advantages:
        - Finding defects earlier in the development cycle
        - Lower cost than dynamic testing
        - CAn be used in all phases of the development cycle
    - Dynamic testing tries to find defects by observing the behavior of the system
    - The different types of dynamic testing include:
        - Functional testing
        - Integration testing
        - Performance testing
        - Security testing
    - Advantages of dynamic testing:
        - Identifying defects that may not be found through static testing
        - Providing real-time feedback on software behavior
        - Can measure system performance and reliability
- **Static Testing Workflow**
    - The Static Testing Workflow is the process of reviewing code before it's executed. 
    - It includes:
        - Code reviews
        - Walkthroughs
        - Inspections

## Test Team Organization
---
### Testing Lifecycle
---
- **STLC**
    - STLC stands for Software Testing Life Cycle. It is a framework for managing the testing process, from planning and design to execution and reporting.
    - Phases:
        - **Requirements Analysis** 
            - Analyze the software requirements and identify the scope of testing.
        - **Test Planning**
            - Create a detailed test plan that outlines:
                - Testing approach
                - Testing objectives
                - Test scenarios
                - Test cases
                - Resource allocation
        - **Test Case Development**
            - Create detailed test cases based on the test plan and requirements.
        - **Test Environment Setup**
            - Set up the necessary hardware, software, and network environments required for testing.
        - **Test Execution** 
            - Execute the test cases and identify any defects or issues.
        - **Test Reporting**
            - Document and report any defects or issues found during testing, along with recommendations for addressing them.
        - **Test Closure** 
            - Prepare the final testing report, summarize the testing process, and provide recommendations for future testing activities.
- **Waterfall Model**
    - The Waterfall Model is a software development methodology that emphasizes a linear and sequential process. 
    - The prior phases must be completed in sequence before moving to the next phase
    - The phases of Waterfall include:
        - Requirements Gathering
        - Design
        - Development
        - Testing
        - Deployment
        - Maintenance
    - Some advantages of the Waterfall Model include:
        - Clear project objectives and deliverables
        - Well-defined roles and responsibilities
        - Predictable project timelines and costs
    - Some disadvantages of the Waterfall Model include:
        - Limited flexibility to change requirements or design
        - Difficulty accommodating changes or feedback from users
        - High risk of discovering defects late in the development process
- **V-Model**
    - The V-Model is an extension of the Waterfall Model that emphasizes verification and validation. 
    - It has a similar set of phases as the waterfall model, but with corresponding testing phases for each development phase
    - There is also a feeback loop from the testing phases back to the developement phase to ensure defects are addressed as early as possible
    - Some advantages of the V-Model include:
        - Increased focus on verification and validation
        - Better alignment of testing with development phases
        - Early detection and resolution of defects
    - Some disadvantages of the V-Model include:
        - Limited flexibility to change requirements or design
        - Difficulty accommodating changes or feedback from users
        - High risk of discovering defects late in the development process
- **Agile Model**
    - The Agile Model is an iterative and incremental approach to software development. 
    - It emphasizes collaboration, felxibility, and rapid feedback
    - It breaks down the development process into small iterations, called sprints, each with a set of goals and deliverables
    - Agile development teams work closely together, including developers, testers, and stakeholders, to ensure the software meets the needs of users
    - Some advantages of the Agile Model include:
        - Flexibility to change requirements or design as needed
        - Better alignment of development with user needs
        - Rapid feedback and continuous improvement
    - Some disadvantages of the Agile Model include:
        - Requires a high level of collaboration and communication
        - May be difficult to estimate project timelines and costs
        - May require more resources than other development methodologies
### Defect Management
---
- **Reporting Defects**
    - Reporting Defects involves documenting and communicating defects found during testing. 
    - It helps to ensure that defects are properly tracked and managed and that the necessary corrective action is taken.
- **Defect Lifecycle**
    - The Defect Lifecycle is the process of identifying, documenting, and resolving defects in software. 
        - Defect Identification
        - Defect Logging
        - Defect Analysis
        - Defect Resolution
        - Defect Verification.
### Tools
---
- **Jira**
    - Jira is a project management tool used for issue tracking, bug fixing, and agile project management
    - It is a platform for teams to plan, track, and release software
    - Key features of Jira:
        - Issue tracking and management
        - Agile project management with Scrum and Kanban boards
        - Customizable workflows and issue types
        - Reporting and dashboards
        - Integration with other development tools such as Git, Jenkins, and Confluence
- **Confluence**
    - Confluence is a collaboration tool for creating, organizing, and sharing knowledge and information
    - Provides a platform for teams to create and share documents, meeting notes, project plans, and other types of content
    - Key features of Confluence:
        - Team collaboration and communication
        - Document and knowledge management
        - Customizable templates for different types of content
        - Search and navigation tools for finding information
        - Integration with other development tools such as Jira and Trello
### Roles
---
- **Review Roles**
    - Review Roles include the author, moderator, and reviewer:
        - **Author** 
            - Responsible for creating the code
        - **Moderator**
            - Responsible for managing the review process
        - **Reviewer**
            - Responsible for identifying defects and providing feedback
- **Test/Developer Independence**
    - Testers should be independent from developers to ensure unbiased testing. 
    - This helps to ensure that defects are properly identified and that
- **Stakeholders and Business Analysts**
    - Stakeholders provide requirements for the software, while business analysts translate those requirements into specifications. 
    - It is important for testers to work closely with stakeholders and business analysts to ensure that the software meets the needs of the user.
- **Tester**
    - The Tester is responsible for designing, executing, and reporting on tests. 
    - They ensure that the software meets the specified requirements and that any defects are properly identified and documented.
- **Test Manager**
    - The Test Manager is responsible for managing the testing process, including creating test plans and strategies, allocating resources, and reporting on progress. 
    - They ensure that the testing is effective, efficient, and meets the desired quality standards.
- **Review Techniques**
    - Review Techniques include walkthroughs and inspections
    - Walkthroughs involve a detailed review of the code by a group of reviewers
    - Inspections involve a more formal process of code review.
### Test Documents
---
- **Test Plan**
    - A Test Plan is a document that outlines the testing strategy and approach.
        - Testing
        - Test Objectives
        - Test Scenarios
        - Test Cases
    - A test plan ensures that testing is carried out in a systematic and organized manner and helps to identify any potential risks or issues before testing begins
- **Test Strategy**
    - A Test Strategy is a high-level plan for testing a software system. 
        - Overall Testing Approach
        - Testing Objectives
        - Testing Timelines
        - Resource Allocation
    - A test strategy helps to ensure that testing is aligned with the overall project goals and objectives
- **Software Requirements Specification**
    - A software requirements specification (SRS) is a document that describes the requirements and specification for a software project
    - It includes:
        - Functional and Non-functional requirements
        - User stories
        - Use cases
        - Acceptance Criteria
    - This serves as a basis for the development of the software and helps to ensure the software meets the requirements set prior
- **Test Progress Report**
    - A test progress report is a document that provides an overview of the testing progress for a software project
    - It includes:
        - Testing status
        - Test cases executed
        - Defects found
        - Test cases pending
    - A test progress report helps to identify any potential issues or delays in the testing process and provides stakeholders with visibility into the testing progress
- **Test Summary Report**
    - A test summary report is a document that provides a summary of the testing results for a software project
    - It includes:
        - Testing objectives
        - Test types and Techniques
        - Testing results
        - Any issues or defects found during testing
    - A test summary report helps to ensure that the software meets the specified requirements and functionality, and provides stakeholders with an overview of the testing results