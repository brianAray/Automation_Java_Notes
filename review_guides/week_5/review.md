# Week 5 Review
## Topics: 
- EC2
- S3
- DevOps
- CodePipeline
- CodeBuild
- CodeDeploy
- Docker
- SonarCloud
- Technical Debt

## Notes
### EC2
- A cloud-based compute service used for creating virtual machines
- Important Components:
    - Amazon Machine Images (AMIs)
    - Elastic Block Store (EBS)
    - Security Groups (SGs)
    - SSH (Secure Shell)
- Use cases:
    - Web Application Hosting
    - Big Data Processing
    - High-performance Computing
    - Dev/Test Environments
    - Media Processing
    - Machine Learning
- AMIs:
 - Pre-configured virtual machine image used to launch an EC2 instance
 - Contains the OS and any additional software and configurations
 - Can use Amazon's pre-built AMIs or create custom AMIs
 - Simplifies the process of autoscaling by allowing easy spin-up of new EC2 instances based on custom AMIs
### S3
 - A cloud-based storage service for objects
 - Objects
    - any file or data that can be stored, including text, images, videos, etc.
 - Use cases:
    - Backup and Recovery
    - Archiving Data
    - Static Website Hosting
    - Analytics
    - Content Delivery
    - Storing logs
- Bucket
    - container for objects stored in S3
- Key
    - unique identifier for an object in S3
- Region
    - physical location of S3 storage
- Access Control List (ACL)
    - controls access to S3 objects
- S3 Lifecycle Policies
    - rules for transitioning objects to different storage classes or deleting them altogether
### DevOps
- A set of practices and tools used for integrating development and operations teams
- Goals:
    - Speeding up the software delivery process
    - Improving software quality
    - Reducing time to market
- Includes:
    - Continuous Integration (CI)
    - Continuous Delivery (CD)
    - Infrastructure as Code (IaC)
    - Automated Testing
    - Monitoring and Logging
### CodePipeline
- A continuous delivery service for building, testing, and deploying code
- Source
    - where the code comes from
- Build
    - where the code is compiled, tested, and packaged
- Test
    - where the code is tested to ensure it meets quality standards
- Deploy
    - where the code is deployed to production
- Stages
    - the phases of the CodePipeline process
- Actions
    - the individual steps in a stage
- Artifacts
    - the output of each stage in the process
### CodeBuild
- A fully managed build service that compiles, tests, and packages code
- Can be integrated with other AWS services, including CodePipeline and CodeDeploy
- Builds can be customized with buildspec.yml files
### CodeDeploy
- A fully managed deployment service for deploying code to EC2 instances, on-premises instances, and Lambda functions
- Deployments can be done in-place or in a blue/green deployment strategy
- Integrates with CodePipeline for automated deployments
### Docker
- A platform for developing, shipping, and running applications in containers
- Containers
    - lightweight, portable, and self-sufficient environments for running applications
- Benefits:
    - Consistency across environments
    - Portability
    - Efficient resource utilization
- Dockerfile
    - file containing instructions for building a Docker image
- Docker image
    - a lightweight, standalone, executable package that includes everything needed to run an application
- Docker container
    - a running instance of a Docker image
### SonarCloud
- A cloud-based code analysis tool for measuring code quality and detecting technical debt
- Provides insights into code quality, security, reliability, and maintainability
- Can be integrated with CI/CD pipelines for automated analysis
### Technical Debt
- The cost of maintaining and fixing software due to poor code quality or design
- Can lead to slower development, increased defects, and higher costs
- Can be managed by:
    - Identifying technical debt early
    - Prioritizing debt based on impact and cost
    - Creating a plan for paying off technical debt over time
    - Maintaining a culture of code quality and continuous improvement