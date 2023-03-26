### Create a Windows baseline image
-----------------------------------

* Install Windows on a computer or virtual machine.  
* Install any required software and updates that you want included in the baseline image. This can include drivers, security software, productivity software, and more.  
* Configure Windows settings, such as user accounts, network settings, power settings, and so on.  
* Install any necessary Windows updates and service packs.  
* Remove any unwanted programs or settings that you do not want included in the baseline image. This can include default programs, bloatware, or any other settings that you do not want included in the final image.  
* Run the Windows System Preparation (Sysprep) tool to prepare the image for duplication. This tool removes any unique system-specific information from the computer, such as the computer name, security identifiers (SIDs), and other unique identifiers. To use Sysprep, follow these steps:  

    a. Open the Command Prompt as an administrator.  
  
    b. Navigate to the Sysprep folder located in %systemroot%\system32\sysprep.  
  
    c. Run the Sysprep.exe file and select the "Enter System Out-of-Box Experience (OOBE)" option. Choose the "Generalize" option to remove system-specific information. Set the "Shutdown Options" to "Shutdown" and click "OK" to run Sysprep.  
  

* Once the computer has shut down, create a disk image of the computer using a disk imaging tool such as Clonezilla, Norton Ghost, or Windows Deployment Services.  
* Save the image to a central location that can be accessed by other computers on the network.  
* Test the image by deploying it to another computer or virtual machine to ensure that it works as expected.  
* If necessary, update the image with additional software or updates, and repeat the Sysprep and imaging process.  

### Build active directory in Windows
-------------------------------------

* Install Windows Server on a computer or virtual machine that will act as the domain controller.  
* Configure the network settings, including the IP address and DNS settings.  
* Install the Active Directory Domain Services (AD DS) role on the server. You can do this through the Server Manager by following these steps:  
  
    a. Open Server Manager and click on "Add roles and features".  
  
    b. Click "Next" on the "Before you begin" screen.  
  
    c. Choose "Role-based or feature-based installation" and click "Next".  
  
    d. Select the server you want to install the AD DS role on and click "Next".  
  
    e. Check the box next to "Active Directory Domain Services" and click "Next".  
          
    f. Click "Next" through the "Features" and "AD DS" screens until you reach the "Confirmation" screen.  
  
    g. Click "Install" to start the installation process.  
  
* Once the AD DS role is installed, you can use the Active Directory Domain Services Configuration Wizard to configure your domain. Follow these steps:  
  
    a. Open Server Manager and click on "AD DS" in the left-hand menu.  
  
    b. Click on "Run the Active Directory Domain Services Installation Wizard".  
  
    c. Choose "Add a new forest" and enter the name of your new domain.  
  
    d. Set the forest and domain functional levels. This determines the features and capabilities that are available in the domain.  
  
    e. Configure the domain controller options, such as the Directory Services Restore Mode password and DNS options.  
  
    f. Review your settings and click "Install" to create the new domain.  
  
* Once the domain is created, you can create organizational units (OUs), user accounts, and other objects in Active Directory Users and Computers. This tool allows you to manage the domain and its users, groups, and computers.  
* You can also configure Group Policy Objects (GPOs) to enforce policies and settings on the domain's computers and users.  
* Once you have set up the domain, you can join other computers to the domain and manage them centrally through Active Directory.  