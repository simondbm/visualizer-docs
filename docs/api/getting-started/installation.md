---
id: installation
title: Installation
sidebar_label: Installation
hide_title: true
---

# Background Service

Processing of models is handled by the DBMVisualizer.BackgroundServices.exe.

## Windows Service

Build DBMVisualizer.BackgroundService project and copy files from the bin/Debug folder to C:\Program Files\DBM Global\Visualizer Background Services.  
Modify DBMVisualizer.BackgroundServices.exe.config to ensure these values are pointing to the correct locations.

```ts
    <add key="RepositoryPath" value="c:\Repository" />
    <add key="APIUrl" value="http://localhost:59258" />
    <add key="TokenAPIUrl" value="https://apptokens.dbmvircon.com/" />
```

## Installing the Background Service

1. Open the **Developer Command Prompt for VS**. 
2. Access the directoy where the compiled executable file is located ie C:\Program Files\DBM Global\Visualizer Background Services and run the command.
3. Run **InstallUtil.exe** from the command prompt with the project's executable as a parameter.

```ts
installutil DBMVisualizer.BackgroundServices.exe
```

## Run the Service

1. Open the Services Manger to check the service has been installed.
2. Right click on the service and click start.
 
![Background Service](/img/api/services.png)

3. Open the Task Manager > Details tab to check the service is running

![Task Manager](/img/api/task-manager.png)

## Message Queuing (MSMQ)

The background service will create a message queue.

1. Open Control Panel.

2. Click Programs and then, under Programs and Features, click Turn Windows Features on and off.

3. Expand Microsoft Message Queue (MSMQ) Server, expand Microsoft Message Queue (MSMQ) Server Core, and then select the check boxes for the following Message Queuing features to install:

- MSMQ Active Directory Domain Services Integration (for computers joined to a Domain).

- MSMQ HTTP Support.

4. Click OK.

5. If you are prompted to restart the computer, click OK to complete the installation.

![windows features](/img/api/bg-service/windows-features.png)

![Task Manager](/img/api/task-manager.png)

1. Open the Computer Management 

### Comments
