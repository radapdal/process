# Deployment Procedures

Step-by-step guide on how to deploy a feature, bug, or a whole website. 


## Terminologies and Definitions


### Environments

**PROD**
- shorthand for "Production" or "Live"
- environment for customers 	
 
 ^
 |

**STAG**
- shorthand for "Staging"
- environment for client changes

 ^
 |

**DEV**
- shorthand for "Development"
- environment for developing and testing new features


### Actions

**PUSH**
- means to deploy changes upwards (DEV -> STAG , STAG -> PROD)

**PULL**
- means to deploy changes downwards (PROD -> STAG, STAG -> DEV)


### Tooltips

<==
==> (***Overwrite***)
- means to overwrite the target environment

<--
--> (***Merge***)
- means to merge to the target environment using a merging tool

</=
=/> (***Manual***)
- means to manually add changes on top of the target environment


### IMPORTANT Guidelines to consider

* The PROD is always in a state of flux, meaning data is always changing and it should be able to at any time.
* Data must go down, changes should come up.
* Pull before you Push.



## Deploying whole Websites

Deploying a website is pretty straightforward as we just need to transfer an existing environment to a directory. But with the important guidelines stated above, this is highly not recommended when pushing towards PROD.

[Initial Deployment Checklist](https://github.com/radapdal/process/blob/master/DeploymentChecklist.xlsx)


### PUSH the whole environment

>  **PROD** <== **STAG** <== **DEV**
>  **PROD** ==> **STAG** ==> **DEV**


### WP Engine hosts

1. Go to WP Engine>Sites>(Site name)>(Environment)>Backup Points. Backup target and source environments.
2. Then in WP Engine>Sites>(Site name)>(Environment), on top right click on "Copy to".
3. Choose the newly added backup point then proceed with the deployment.


### Non-WP Engine hosts

This procedure will use the plugin [Migrate Guru](https://wordpress.org/plugins/migrate-guru/) and is only applicable to it's supported hosts.

1. Open both target and source websites then backup both using the backup plugin.
2. On the source, go to Migrate Guru. Register or login to start migration.
3. Select target Host. Fill in migration form with target environment's settings, then hit "Migrate".



## Adding and Deploying select changes

Deploying select changes is the most tedious process which will depend on a lot of factors. 


### WPMerge.io

WPMerge.io is a premium plugin that solves the problem of merging two databases by tracking changes on the STAG and applying it on top of changes from PROD. This follows the guidelines stated above.

#### PULL PROD then PUSH changes

>  **PROD** --> **STAG**
>  **PROD** <-- **STAG**

1. In STAG go to WPMerge.
2. Click on "Clone Prod DB & Apply Dev Changes" to Pull.
3. Add your changes.
4. When ready to Push, set the PROD to maintenance.
5. Go back to STAG>WPMerge, and click on "Clone PROD DB & Test Merge". 
5. Check for data inconsistencies like duplicates.
6. After the verification, click on "Apply Dev Changes to Prod" and wait for the process to complete.
7. Click on "Download files as a zip" and complete the download.
8. Open zip file and transfer files to PROD using FTP.
9. Verify deployment in PROD.
10. When ready, remove site from maintenance.
11. Go back to STAG>WPMerge, then click on "Clone PROD DB & Test Merge" to start tracking again.


