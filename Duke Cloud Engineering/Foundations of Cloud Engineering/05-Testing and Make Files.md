# Testing
Testing is a critical aspect of software development that can help identify and resolve problems. One important concept in testing is the creation of a simulated environment where production processes can be replicated.

This allows developers to observe the system's behavior in a controlled setting and identify potential issues. Instrumentation and monitoring, such as logging and dashboards, are essential components of testing as they provide insights into the system's operations and help pinpoint critical failure points. A successful testing strategy involves finding a balance between too much and too little testing.

> [!Warning]
>Blindly pursuing 100% test coverage or excessive functional tests can be counterproductive

## Types of Tests

- Unit tests operate at a low level.
- Integration tests focus on ensuring different modules or services work together harmoniously.
- Functional tests verify that an application fulfills its business requirements. 
- End-to-end testing replicates user behavior to test the entire system.
- Acceptance testing provides a structured method to confirm specific functionalities. 
- Performance testing, sometimes called load testing, examines an application's performance under stress.
- Sanity testing, often used with exploratory data analysis, offers a basic check to ensure things are functioning as expected.

# Makefiles
A Makefile is a file that automates tasks in a software project, particularly build and testing processes. Instead of manually typing out long commands. 

Makefiles allow developers to execute them with simpler commands like "make lint." This automation simplifies workflows and reduces errors.

## Related Notes

- [[03-CI and CD]]