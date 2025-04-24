# Start-SPOSiteAccessReview
Kick off SharePoint Site Access Review

## DESCRIPTION

This cmdlet is used to generate site access reviews for SharePoint Online. It reads siteId ID's from a text file and generates site access reviews for each siteId id found. The script also checks if the required modules are installed and imports them if necessary. It handles errors and logs the output to a specified directory.

## How to get started with Start-SPOSiteAccessReview

1. Download this in to a directory of your choice
2. Navigate to that directory and run run: Import-Module -Name .\Start-SPOSiteAccessReview.ps1 (this will import in to the local PowerShell session)
3. Run one of the examples below and allow for tab completion to see all of the available options

## EXAMPLE 1
    C:\PS> Start-SPOSiteAccessReview -TenantDomain contoso -siteIdID e4525a99-781c-437c-b4fa-2335cf9142a9 -InputFilePath C:\temp\siteids.txt

    This will read in all of the siteId IDs from the file c:\temp\siteIds.txt and generate a site access review for each of them.

## EXAMPLE 2
    C:\PS> start-SPOSiteAccessReview -TenantDomain contoso -siteIdID e4525a99-781c-437c-b4fa-2335cf9142a9 -InputFilePath C:\temp\siteids.txt -DisconnectFromSPO

    This will read in all of the siteId IDs from the file c:\temp\siteIds.txt and generate a site access review for each of them and disconnect from SharePoint Online.

## NOTES
If you are using a text file it should contain a list of site IDs, one per line. If using a .csv file, it should contain a column named "SiteID" and put all siteId's in the first field.

- For more information please see: https://learn.microsoft.com/en-us/powershell/module/sharepoint-online/start-spositereview?view=sharepoint-ps
- This script will install both the Microsoft.Online.SharePoint.PowerShell and ExchangeOnlineManagement modules if they are not installed.
- Default logging directory is c:\users\username\Documents\SamsiteIdingLogs.txt