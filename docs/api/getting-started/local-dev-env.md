---
id: local-dev-env
title: Local Dev Environment
sidebar_label: Local Dev Environment
hide_title: true
---

# Local Development Environment

To Get Started with the DBM Visualizer Project......

## Prerequisites

- Visual Studio 2019
- .NETFramework, Version=v4.7
- SQL Server 2019 Developer Edition
- Microsoft SQL Server Management Studio

## Clone Repository

Clone the Visualizer Repository from Visual Studio by going to the Git>Clone Repository and select the Azure DevOps option under Browse a repository.

![Clone Repository](/img/api/local-dev-env/clone-repo.png)

From the Connect to a Project dialog select DBM Visualizer and clone to Path: C:\DBMV\DBM Visualizer

![Clone Repository](/img/api/local-dev-env/connect-to-azure.png)

From the Git Changes View switch to the develop branch.

![Clone Repository](/img/api/local-dev-env/dev-branch.png)

Set VisualizerAPI and DBMVisualizer as Multiple startup projects.

![Startup Projects](/img/api/local-dev-env/startup-projects.png)

## Database

- Request a database backup from a team member along with a copy or their local Repository.
- Restore database
- Ensure user has access to the database

![SQL Login](/img/api/local-dev-env/sql-login.png)

 - Check dbo_MigrationHistory is the same in the project <strong>DBMVisualizer.Data</strong>. If the project is ahead of the db, build the project and run. Also from the package-manager console in visual studio run the command 
 ```
 update-datebase.
 ```

## Repository

When working in Development, a local Repository is required to store models as we won't be using the online storage server.
Under the C: drive create a Repository directory. At the root of the directory, folders are created for each of the CompanyId(Guid).

![Repository](/img/api/local-dev-env/c-repository.png)

### Models

Models are downloaded to C:/Repository/(CompanyId)/(ProjectID)/(ModelID)/

![Repository](/img/api/local-dev-env/models.png)

### Comments
