### Create dynamic group in Azure
---------------------------------

* Sign in to the Azure portal (https://portal.azure.com) with your Azure AD administrator credentials.  
* In the left-hand menu, click on "Azure Active Directory".  
* Click on "Groups" in the left-hand menu.  
* Click on the "+ New group" button at the top of the page.  
* In the "Group type" dropdown, select "Dynamic device" or "Dynamic user", depending on whether you want to create a group based on devices or users.  
* In the "Name" field, enter a name for the group.  
* In the "Membership type" dropdown, select "Dynamic".  
* In the "Rules" section, define the criteria for the dynamic group based on attributes of the devices or users. You can use a wide variety of attributes, such as job title, department, location, device type, and more. Here's an example rule for a dynamic user group that includes all users with a job title of "Manager":  
```
user.jobTitle -eq "Manager"
```  
* Click the "Save" button to create the dynamic group.  
* You can now use the dynamic group to assign policies, licenses, or other settings to all the devices or users that match the group criteria.  