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

<b>1.	CodeCommit Setup</b><br>
a. Create a CodeCommit repository to store the source code.
<img src="https://github.com/Jackiedee1223/CloudDevOps-3/tree/main/images/CodeCommit.PNG">
b. Create an IAM user with appropriate permissions for CodeCommit.
<img src="https://github.com/Jackiedee1223/CloudDevOps-3/tree/main/images/IAM.PNG">
<img src="https://github.com/Jackiedee1223/CloudDevOps-3/tree/main/images/ARN.PNG">
<img src="https://github.com/Jackiedee1223/CloudDevOps-3/tree/main/images/Policy.PNG">
c. Generate SSH keys locally and associate them with the IAM user for secure access.
    <b>ssh-keygen</b>
<img src="https://github.com/Jackiedee1223/CloudDevOps-3/blob/main/images/CodeCommit.PNG">
d. Transfer the source code from the existing GitHub repository to the CodeCommit repository and push the changes.
<img src="https://github.com/Jackiedee1223/CloudDevOps-3/blob/main/images/CodeCommit.PNG">




<h2>Reference</h2>
<p>Learning from <b>GURUTECH NETWORKS</b> </p>
