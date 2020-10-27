Cleanup SQL Server Firewall Rules and Log to Application Insights
=================================================================

            

**Description**


This runbook is designed to purge Azure SQL Server firewall rules not specified on a defined safe list & log the outcome in App Insights for audit purposes. A runbook like this should be implemented to regularly delete whitelisted IP addresses as standard
 security practice.


For this runbook to work, the SQL Server must be accessible from the runbook worker running this runbook. Make sure the SQL Server allows incoming connections from Azure services by selecting 'Allow Windows Azure Services' on the SQL Server configuration
 page in Azure. Consequently, this rule that allows Azure IP addresses is excluded from the purge.


**Requirements**


An Azure 'RunAsAccount' needs to be created for the Automation account. Documentation can be found
[here](https://docs.microsoft.com/en-us/azure/automation/manage-runas-account#create-a-run-as-account-in-the-portal)


Finally, to log to Applications Insights, the Custom Events Module ('ApplicationInsightsCustomEvents.zip') must be imported in the Automation account under the 'Modules' pane. The zip file can be found [here](https://gallery.technet.microsoft.com/scriptcenter/Log-Custom-Events-into-847900d7)


**Runbook Content**


The runbook contents are displayed below


 

 

        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
