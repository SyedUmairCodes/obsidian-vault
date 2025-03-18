# Continuous Integration
Continuous Integration (CI) is a software development practice that ensures your software is always in a known, working state. This approach saves time and allows for quicker development cycles. 

> One of the key benefits of CI is that it provides a safety net, much like a seat-belt in a car, allowing developers to work quickly with the assurance that their code is being continuously tested.

Essentially, CI automates the repetitive process of manually testing code, similar to how car factories automate car manufacturing.1 This automation ensures that the code base is consistently in a known state, saving developers time and reducing the risk of errors.

---
# Continuous delivery
Continuous delivery (CD) is a software engineering best practice where code is always maintained in a deployable state, encompassing both the application code and its underlying infrastructure. 
## How Continuous Delivery Works
Developers make changes to the codebase and commit them to a source control repository. The master branch (or a designated branch) is typically linked to a specific environment.

When code is pushed to the linked branch, a build server is automatically triggered. The build server initiates a series of automated steps:

- The server integrates the latest code changes and builds the application.
- Automated tests are executed to ensure code quality and functionality.
- The build server, using infrastructure-as-code tools like Terraform or CloudFormation, checks and updates the infrastructure required for the application. 
- The application is deployed to the designated environment associated with the branch.

Different branches in the source control repository can be mapped to corresponding environments. This allows for isolated testing and staged deployments.

## Related Notes