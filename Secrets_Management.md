# Best Practices for Securing on CI/CD

## CI/CD Pipeline
CI/CD is a widely used software engineering practice that combines continuous integration (CI) processes with continuous delivery (CD) or continuous deployment (CD) processes to accelerate the development and deployment of software applications. A CI/CD pipeline is a collection of tools used by developers, test engineers and IT operations staff throughout the continuous software development, delivery and deployment lifecycle. Popular CI/CD tools include CloudBees, Jenkins, Azure DevOps, Bamboo and Team City
##C I/CD Pipeline Privileged Access Security Challenges
The CI/CD pipeline includes a variety of on-premises and cloud-based resources used to build, test and run code. Each platform in the CI/CD toolchain requires secrets and privileged credentials to access other resources, including other tools, to pull code from repositories, etc. While most tools have some form of native build in capability to secure credentials, the capabilities vary widely. For example, many tools cannot rotate secrets or track their usage for audit. Additionally, when secrets are maintained and administered using different tools and processes, this not only creates additional security gaps and vulnerabilities but also leads to secrets sprawl (e.g., the same secret is replicated in multiple places). Moreover, too often secrets and cloud credentials are hardcoded, which makes then effectively almost impossible to rotate and change. And there have been too many instances of code placed in repositors by developers expecting the code to be private but then inadvertently tagged as public — exposing the credentials to attackers who specifically crawl code repositories searching and stealing inadvertently exposed credentials.

## CI/CD Pipeline Secrets Management Challenges
The CI/CD pipeline is an integral component of the modern software supply chain and is subject to a wide variety of security threats and risks — from code, malware and artifact injection, to hijacked IT resources, stolen intellectual property and code theft. CI/CD environments are often complex, highly distributed and potentially complicated to secure.
The secrets — passwords, SSH keys, API keys, cloud access keys — CI/CD tools, applications and microservices use to access systems and secure transactions are dispersed across machines and clouds, making them difficult to track and manage.

## Best Practices for Securing the CI/CD Pipeline
CI/CD requires a fresh approach to security — a centralized approach that unifies secrets management and centralizes privileged access controls. Examples of best practices to improve the security of the CI/CD pipeline include:

- Implementing a secrets management solution to centrally secure, manage and rotate secrets used by the CI/CD pipeline, the tool chain and the credentials needed to access code repositories, cloud platforms, etc. With a centralized secrets management solution, secrets can be stored in a tamper-resistant digital vault, removed from source-code repositories.
- Using a privileged access management solution to enforce least privilege access to all CI/CD platforms.
- Automatically rotating secrets and privileged access credentials regularly or on demand.
- Monitoring and tracking privileged access activity for both administrators and automated users.
- Employing multi-factor authentication (MFA) to prevent sensitive scripts from running automatically and forcing human intervention to review or approve actions like pushing commits to Git

[Demo video - Securing CI/CD pipeline](https://www.youtube.com/watch?v=8mUijkxvi-4)
- This demo video aims to provide 2 scenarios: one CI/CD pipeline with hardcoded secrets, and the one is secreted by Conjur
