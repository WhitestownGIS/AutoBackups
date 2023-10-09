# AutoBackups
The Inspiration: A land parcel feature service layer maintained by the county that overrides its data each time a change is made, which fails to preserve parent parcels and their related data fields. 

The Goal: To automatically save weekly backups of all online feature layers. 

The Process: 
1. Develop an arcpy script that will save the current layer with the date in its field name. This script runs in a python notebook saved in an ArcGIS Pro project that contains the online layers of interest.
2. Create a Power Automate flow to run the script. It also must save the file to a shared OneDrive location where all backups will be stored, and can be sorted by date. For a detailed desricption visit https://github.com/WhitestownGIS/AutoBackups.wiki.git
3. Develop an AutoIt script to start the Power Automate flow automatically.
4. Create a scheduled task using Windows Task Scheduler to run the AutoIt script at the same time every week.

The Results: A population of files that record weekly changes in our online feature layers without any user interference.

