# AutoBackups
The Problem: A land parcel layer maintained by the local county that overrides its geometry and tabular data with every update, failing to preserve parent parcels and their related data fields. 

The Goal: To create an automatic process that saves weekly backups of all important online feature layers. 

The Process: 
1. Develop an arcpy script that will save the current layer with the date in its field name. This script runs in a python notebook within an ArcGIS Pro project that contains the online layers of       interest.
2. Create a Power Automate flow to run the script, and save the backup. It must save the file to a shared OneDrive location where all backups will be stored, and sorted by date. For a detailed 
   desricption of this flow visit our Wiki page.
3. Develop an AutoIt script to start the Power Automate flow automatically.
4. Create a scheduled task using Windows Task Scheduler to run the AutoIt script at the same time every week.

The Results: A population of files that record weekly changes in our online feature layers without any user interference.


Requirements: 
-ArcGIS Pro
-AutoIT
-Windows Task Scheduler
