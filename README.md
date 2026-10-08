Mini Production Test
Project Purpose

This repository is a small production-style project created to practice Git and GitHub workflows used in real development environments.

The project contains a sample application configuration, application health information, deployment status information, and Git configuration files.
Project Structure

.
├── README.md       # Project documentation
├── app.txt         # Sample application/configuration
├── status.txt      # Production status information
├── health.txt      # Application health information
└── .gitignore      # Files ignored by Git

Setup

Clone the repository:

git clone git@github.com:parvezmahmud22/Mini-production-test-.git
cd Mini-production-test-

Check the project files:

ls -la

Review the application configuration:

cat app.txt

Check the application status:

cat status.txt

Check the health information:

cat health.txt

Testing

The project can be tested by checking the configuration, status, and health files.

Run:

cat app.txt
cat status.txt
cat health.txt

The expected health result is:

Overall Status: PASS

Git Workflow

The following Git workflow was followed:

    Created the repository and initialized the project.
    Created the main branch as the primary branch.
    Added the initial project files.
    Created meaningful commits for different changes.
    Created a feature branch for an additional project improvement.
    Committed the feature separately.
    Pushed the feature branch to GitHub.
    Opened a Pull Request from the feature branch to main.
    Reviewed and merged the Pull Request.
    Updated the local main branch after the merge.

The workflow was based on:

main
  |
  +---- feature branch
           |
           +---- changes
           |
           +---- Pull Request
                    |
                    +---- merge
                           |
                           v
                          main

Production Challenge

The production challenge was to make a small repository behave like a real project instead of containing only application files.

During the challenge, the repository was organized with documentation, configuration, health information, status information, and a .gitignore file.

An important part of the challenge was configuring GitHub authentication. Initially, GitHub rejected SSH authentication with a Permission denied (publickey) error. An ED25519 SSH key was generated and added to the SSH agent and GitHub account. After configuring SSH authentication, the repository could be accessed using the GitHub SSH remote.

This demonstrated the importance of:

    Git repository organization
    Meaningful commits
    Feature branches
    Pull Requests
    Production health checks
    Secure GitHub authentication
    Keeping unnecessary files out of version control

Production Status

Current application status:

Application: Operational
Environment: Production
Version: 1.0.0
Health: PASS

Conclusion

This mini production repository demonstrates a basic real-world Git workflow from development through feature branching, Pull Request review, merging, and production-style status checking.
