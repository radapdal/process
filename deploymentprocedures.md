# Deployment Procedures

Step-by-step guide on how to complete the [Deployment Checklist](https://github.com/radapdal/process/blob/master/DeploymentChecklist.xlsx)


### 1. Back up production and development

1.1. Login to production as admin. 

1.2. In the top admin bar, select UpdraftPlus > Backup/Restore.

1.3. Click the big blue "Backup Now" button.

1.4. Wait until the process complete. Do the same for the development site.

### 2. Create new database and assign user

2.1. Login to the production cPanel.

    If there is no cPanel account, login to the Hosting account and open the cPanel from there.

2.2. Find the "Databases" section, click on MySQL Databases.

2.3. In "Create New Database", add an appropriate name and click on "Create".

2.4. Below in "Add User To Database" choose the admin user, ex. yempo_admin, and choose the new database created. Click on "Add", this will redirect you to the user privileges page.

2.5. In the list of privileges for the database user, select "ALL PRIVILEGES". Click on "Make Changes".

### 3. Create Duplicator package

3.1. In the development admin dashboard, select "Duplicator".

3.2. In the Packages list, click on  "Create New".

3.3. 
