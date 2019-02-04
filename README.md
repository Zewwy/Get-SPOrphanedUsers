# Get-SPOrphanedUsers
SharePoint Script to create a list of Orphaned Users

This script is written to simply take, save, and run.

It will ask you for all required parameters to complete, and do validation checking along the way.

It first asks for a SharePoint Web Application. (Expecting to be run on the SP mgmt console)

Then ask for a domain trust if users are required to be tested agaist a trust domain forest.
If nothing is entered the forest domain in which the front end server is joined is used.

Then you can filter for certain domains as when you have a forest trust users will not return as users as they are in the other domain.

Then it will ask how you would like the results displayed: Console or Log or both
