up:: [[Computer Science MOC]]
tags:: #Programming  
# CD (Continuous Deployment)
- An extension of [[CI Tools]]
	- Automates the release of code changes to production. 
- Every change that passes all stages of the production pipeline is released to customers automatically.
- **Purpose**: The aim is to *reduce the time it takes to release new software* features and bug fixes, ensuring that code is always in a deployable state and can be released frequently and reliably.
- **Key Practices**:
    - Automated Deployment: Changes are automatically deployed to production after passing all tests.
    - Monitoring: Continuous monitoring of the application in production to ensure it operates correctly.
    - Rollbacks: Implementing mechanisms to quickly revert to a previous version if issues are detected in production.
- **CD Tools**: Spinnaker, Argo CD, Harness