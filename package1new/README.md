# Infrastructure as Code (IaC) Home

Welcome to the Infrastructure as Code (IaC) repository. _Infrastructure Prime_ is the monolithic repository (monorepo) for all IaC deployments. This repository is dedicated to managing and orchestrating the infrastructure setup across various platforms including Docker, AWS, Azure, and Oracle. Our goal is to streamline development processes and ensure consistency across all environments.

## Purpose

The IaC repository serves as the central hub for all infrastructure coding efforts. By using this monorepo structure, we aim to:

- **Centralize Management**: Single repository for all infrastructure configurations makes it easier to manage permissions, dependencies, and updates.
- **Improve Collaboration**: Teams can work together more effectively with shared contexts and easier code reviews.
- **Consistency and Standardization**: Ensure uniform standards across all infrastructure deployments, reducing the chances of discrepancies.
- **Enhanced Security**: Simplify security protocols by concentrating all infrastructure code into a single repository.

## Repository Structure

The repository is organized by technology stack and deployment environments as follows:

```
infrastructure-prime/
│
├── common/              # Common configurations and scripts shared across platforms
│
├── docker/              # Docker configurations and environments
│   ├── common/          # Reusable components for across all Docker-based IaC
│   └── anything-llm/    # AnythingLLM docker IaC     
│   └── vanna-ai/        # Vanna AI SQL agent docker IaC
│   └── litellm-proxy/   # OpenAI proxy server docker IaC
│   └── glide/           # LLM Gateway docker IaC
│
├── aws/                 # AWS (Amazon Web Services) infrastructure
│   ├── common/  # Reusable components for across all AWS IaC
│   └── <whatever other deployments>/  # AWS-based deployments using CDK
│
├── azure/               # Microsoft Azure infrastructure
│   └── <whatever other deployments>/  # Various deployments on Azure
│
├── oracle/              # Oracle Cloud infrastructure
│   ├── <whatever other deployments>/  # General Oracle Cloud deployments
│   └── virtualbox/      # VirtualBox environments managed in any local or hosted VMs
│       └── sandbox/     # Sandbox environment for VirtualBox setups
│
├── utils/               # Utilities and scripts
    ├── cli/             # Command line utilities
       └── baml/         # BAML LLM function command line utility
```

### Directory Descriptions

- **Common**: Contains scripts, templates, and configurations that are used across multiple platforms to ensure consistency and reduce duplication.
- **Docker**: Contains Dockerfiles and related scripts for creating and managing Docker containers, particularly for development and testing environments.
- **AWS**: Houses templates and scripts for deploying services on AWS using the Cloud Development Kit (CDK). This includes specific deployments like synthetic SFTP servers as well as templates for scalable cloud architectures.
- **Azure**: Includes configurations and deployment scripts for services hosted on Microsoft Azure, covering a range of applications from web services to database configurations.
- **Oracle**: Contains Oracle Cloud-specific deployments and configurations, including setups for VirtualBox that facilitate isolated environments for testing and development within Oracle Cloud.

## Getting Started

To get started with using or contributing to the IaC repository, please ensure you have the following prerequisites:

1. Access to the GitHub account.
2. Proper setup of necessary tools and access credentials for Docker, AWS, Azure, and Oracle Cloud.
3. Familiarity with Git and GitHub workflows.

Clone this repository using:
```
git clone https://github.com/netspective/healthelink-ai-expr-IaC-prime.git
```

## Contribution Guidelines

Contributions to the IaC repo are welcome! Please follow our contribution guidelines:

- **Code Reviews**: All commits should be made via pull requests and reviewed by at least one other team member.
- **Style Guide**: Adhere to the coding styles and guidelines provided in the `docs/` directory.
- **Issue Tracking**: Use GitHub Issues to track tasks and bugs.
- **Branch Naming**: Follow the branch naming convention `feature/<feature>`, `bugfix/<issue>`, or `hotfix/<issue>` for clarity and organization.

## License

This project is licensed under the [MIT License](LICENSE.md).

For more information or to report an issue, please contact the infrastructure team at `(...fill this out...)`.

Thank you for being part of our project!
