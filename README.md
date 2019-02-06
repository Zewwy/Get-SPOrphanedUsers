# Get-SPOrphanedUsers
SharePoint Script to create a list of Orphaned Users

This script is written to simply take, save, and run.

It will ask you for all required parameters to complete, and do validation checking along the way.

It first asks for a SharePoint Web Application. (Expecting to be run on the SP mgmt console)

Then ask for a domain trust if users are required to be tested agaist a trust domain forest.
If nothing is entered the forest domain in which the front end server is joined is used.

Then you can filter for certain domains as when you have a forest trust users will not return as users as they are in the other domain.

Then it will ask how you would like the results displayed: Console or Log or both (Both hasn't yet been implemented yet lol)

If Log is chosen you will then be asked how you would like the log file saved (text/csv/xml)

Then enter a file name (this can either be fully qualified, of just a name and the location where the script is run will be used).

*Note*

I removed the .AllWebs | Foreach-Object as I found every subsite always contained the same users as the RootWeb
So I instead used a variable in place of each objects $_ specifying the root web with .AllWebs[0]  (I probably could also accomplish this with .RootWeb)

But ¯\\_(Oo)_/¯

Enjoy.
