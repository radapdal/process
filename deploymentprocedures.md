# Deployment Procedures

Step-by-step guide on how to complete the [Deployment Checklist](https://github.com/radapdal/process/blob/master/DeploymentChecklist.xlsx)


Tooltip:
* --> (***Merge***)
* => (***Overwrite***)

#### PUSH

> **DEV** --> **STAG** => **PROD**

#### PULL

> **PROD** => **DEV** --> **STAG**



## Non-WP Engine Servers

### Push

#### 1. Back up environments

1.1. Login to PROD as Admin. 

1.2. In the top Admin bar, select UpdraftPlus > Backup/Restore.

1.3. Click the big blue "Backup Now" button.

1.4. Do the same for the STAG site. Wait until the process completes. 



#### 2. Create Duplicator package

3.1. In the STAG Admin menu, select "Duplicator".

3.2. In the Packages list, click on  "Create New".

3.3. 
