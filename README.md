# Continuous Integration of on AWS Cloud
<h2>Scenario</h2>
<p>
In the fast-paced world of software development, where Agile methodologies are the norm, continuous improvement is the key to success. In our Cloud DevOps Project, we address the challenges associated with the traditional Build & Release process, highlighting the inefficiencies in testing and the resultant accumulation of bugs and errors. To mitigate these issues, we introduce the concept of Continuous Integration (CI) on the AWS Cloud, transforming the development landscape for better agility and efficiency.

In an Agile Software Development Life Cycle (SDLC), developers regularly make code changes, leading to the need for frequent builds and tests. Traditionally, Build & Release teams or developers themselves undertake these tasks. However, the manual nature of this process often results in infrequent testing, leading to the accumulation of bugs and errors that demand rework. Additionally, inter-team dependencies and manual interventions further hinder the development flow.

Frequent code changes in an Agile SDLC demand equally frequent testing to ensure the reliability of the codebase. The manual Build & Release process often becomes a bottleneck, slowing down the development cycle. This results in delayed bug identification and resolution, leading to increased rework for developers. The presence of inter-team dependencies further complicates matters.

To address these challenges, we propose a paradigm shift towards Continuous Integration (CI) – a development practice that requires developers to integrate code changes into a shared repository several times a day. With every commit triggering an automated build and test process, developers receive instant feedback on the quality of their code. This not only reduces the Mean Time to Recovery (MTTR) but also promotes an agile and fault-isolated development environment.

In our quest for an optimal CI setup, we leverage various AWS services tailored for each phase of the CI/CD pipeline. CodeCommit serves as our version control system, while CodeArtifact manages Maven repositories for dependencies. CodeBuild handles the build process, CodeDeploy facilitates artifact deployment, and CodePipeline integrates these components seamlessly. Additionally, SonarCloud and Checkstyle contribute to code analysis and quality checks.

By transitioning to Continuous Integration on the AWS Cloud, our project aims to streamline the development process, significantly reduce manual interventions, and enhance overall agility. With this innovative approach, we embrace a new era of development where code changes are validated continuously, leading to faster delivery, improved code quality, and a more collaborative and efficient development environment.
</p>

<h2>Architecture of AWS Services</h2>
 <img src="https://github.com/Jackiedee1223/image-repos/blob/main/CloudDevOps-3.png">

<h2>Flow of Execution</h2>

1.	Create Key pair for Beanstalk instance login: Generate a key pair that will be used for secure login to Elastic Beanstalk instance.
2. Create Security Group for Amazon ElastiCache, RDS, and ActiveMQ: Define security groups to control inbound and outbound traffic for ElastiCache, RDS, and ActiveMQ instances.	 
3.	Create RDS, Amazon ElastiCache, and Amazon ActiveMQ: Set up relational database (RDS), caching with ElastiCache, and the message broker with ActiveMQ.
4.	Create Elastic Beanstalk Environment: Deploy and manage the application in an Elastic Beanstalk environment, allowing automatic scaling and easy application management.
5. Update SG of backend to allow traffic from Bean SG: Adjust security group rules to permit traffic from Elastic Beanstalk security group to the backend services.	
6.	Update SG of backend to allow internal traffic: Configure security groups to enable internal communication between components.
7.	Launch EC2 instance for DB initializing: Start an EC2 instance dedicated to initializing and configuring RDS database.
8. Login to the instance and initialize RDS DB: Access the EC2 instance to execute the necessary scripts or commands to initialize RDS database.	
9.	Change health check on Beanstalk to login: Adjust the health check settings on Elastic Beanstalk to ensure it checks the login status or relevant indicators.
10.	Add 443 https Listener to ELB: Enhance security by configuring a secure HTTPS listener on Elastic Load Balancer (ELB).
11. Build Artifact with Backend Information: Compile an artifact containing the necessary information for the backend services.
12. Deploy Artifact to Beanstalk: Use Elastic Beanstalk to deploy the compiled artifact, making the application available.
13. Create CDN with SSL Cert: Establish a Content Delivery Network (CDN) and configure it with an SSL certificate for enhanced performance and security.
14. Update Entry in GoDaddy DNS Zones: Update the DNS settings in GoDaddy account to point to the newly created CDN and ensure proper domain resolution.
15. Test the URL: Conduct thorough testing to verify that the application is accessible and functioning correctly through the updated URL.




<h2>Validation & Summarization</h2>
<h4>Security Group & Key Pairs</h4>
<h4>EC2 Instances</h4>
<h4>Build and Deploy Artifacts</h4>
<h4>Load Balancer & DNS</h4>
<h4>Auto Scaling Group</h4>













<h2>Reference</h2>
<p>Learning from <b>GURUTECH NETWORKS</b> </p>
