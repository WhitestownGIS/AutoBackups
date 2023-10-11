# AutoBackups
The Problem: A feature service layer maintained by the county that overrides its geometry and tabular data with each update, failing to preserve parent polygons and their related data fields. 

The Goal: To create an automatic process that saves regular backups of all important online feature layers. 

The Process: 
1. Develop an arcpy script that will save the current layer with the date in its field name. This script runs in a python notebook within an ArcGIS Pro project. The project contains all the online     layers of interest.
2. Create a Power Automate flow to run the script, and save the backup. It must also copy the file(s) to a shared OneDrive location where all backups will be stored, and sorted by date. For a          detailed desricption of this flow visit our Wiki page.
3. Develop an AutoIt script to run the Power Automate flow automatically.
4. Create a scheduled task in Windows Task Scheduler to trigger the AutoIt script each week at the same time.

The Results: A population of files that record weekly changes in our online feature layers without any user interference.


Requirements: ArcGIS Pro, AutoIt, Power Automate, and Windows Task Scheduler
