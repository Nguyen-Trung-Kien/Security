# Ci/Cd concept

## What is VCS

A Version Control System (VCS) is a tool or system that helps manage and track changes to a project's source code. It allows multiple developers to work together on the same project without losing or

### Features of VCS

* **Version Management**: Tracks and stores different versions of the source code.
* **Restoration**: Allows reverting to previous versions of the code if needed.
* **Change Tracking**: Records who made what changes and when.
* **Branching and Merging**: Supports working on different branches of the project and merging changes from different branches back into the main branch.

### Common VCS

* Git: most popular VCS tools, commonly used with platforms like GitHub, GitLab, and Bitbucket.
* SVN: Often used in businesses, but is now decreasing.

## What is pipeline

a **pipeline** refers to an automated series of steps that manage the lifecycle of code changes from development to deployment.

In short, a pipeline is a set of pre-written automated steps to perform delivery, testing, deployment, etc.

### Key components of CI/CD pipelines <a href="#key-components-of-cicd-pipelines" id="key-components-of-cicd-pipelines"></a>

#### Config File

Configuration files are stored in your code repository and are written in declarative YAML code. This configuration-as-code approach allows teams to manage their pipeline definitions right alongside their application code, adding transparency and traceability to pipeline management.

CI/CD pipeline configuration files allow you to define the jobs you want performed, the order in which they should occur, and the execution environment in which they should run. Let’s take a closer look at each of these components.

* **Jobs and steps**: are the basic units of work in a CI/CD pipeline. You can define specific requirements for each job, such as the runtime environment and the resources needed
* **Workflows**: Workflows define the rules that govern the execution order of jobs and can include conditions under which certain jobs should be triggered. They allow you to specify dependencies between jobs, ensuring that they run in the proper sequence

