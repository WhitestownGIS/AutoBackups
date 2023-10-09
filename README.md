# AutoBackups
The Inspiration: The county feature service layer overrides its data each time a change is made, which fails to preserve parent parcels and their related data fields. 
The Goal: To automatically save weekly backups of all online feature layers, inspired by the parcel layer. In that case, giving us the information to track parent parcels and develop historic layers. 

The Process: 
1. Develop an arcpy script that will save the current layer with the date in its field name. This script runs in a python notebook saved in an ArcGIS Pro project that contains the online layers of interest.
2. Create a Power Automate flow to run the script. It also must save the file to a shared OneDrive location where all backups will be stored, and can be sorted by date.
3. Develop an AutoIt script to start the Power Automate flow automatically.
4. Create a scheduled task using Windows Task Scheduler to run the AutoIt script at the same time every week.

The Results: the population of files that record weekly changes in our online feature layers without any user interference.

