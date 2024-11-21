<h1>Home Lab Active Directory Using Oracle Virtual Box</h1>

![](https://github.com/rbrianshutt/nessus/blob/main/images/NessusEssentials.jpg)

<h2>Description</h2>
x  
<br />


<h2>Technology Used</h2>

- <b>VMware Workstation Pro</b>
- <b>Windows 10 ISO</b>
- <b>Nessus Essentials</b>
- <b>Old version of Firefox</b>

 
<h2>Program walk-through:</h2>


- <b>Installed VMware Workstation Pro</b>
- <b>Download Windows 10 ISO</b>
- <b>Download and Install Nessus Essentials</b>
- <b>Connect with VM</b>
<br/>
<b>Set up a basic scan in Nessus Essential</b>
<br/>
<br/>
 
![](https://github.com/rbrianshutt/nessus/blob/main/images/basic_network_scan.PNG)
<br />
<br />
<b>Create a new scan.  Connect Nessus with host IP address: </b>
<br/>

![](https://github.com/rbrianshutt/nessus/blob/main/images/new_scan_basic_network_scan.PNG)
<br />
<br />
<b>Initiate scan:</b>  
<br/>
![](https://github.com/rbrianshutt/nessus/blob/main/images/launch_scan_2.PNG)
<br />
<br />
<b>Results for scan without credentials:</b>  
<br/>
![](https://github.com/rbrianshutt/nessus/blob/main/images/nessus_first_scan.PNG)
<br />
<br />
<b>Configure Nessus for credentials of host VM:</b> 
<br/>

![](https://github.com/rbrianshutt/nessus/blob/main/images/nessuss_configure_credentials.PNG)
<br />
<br />
<b>Enable remote registry, set to Automatic:</b>   
<br/>
![](https://github.com/rbrianshutt/nessus/blob/main/images/vm_enable_remote_registry.PNG)
<br />
<br />
<b>Perform another scan, but with credentials.  The results return more vulnerabilities.</b>  
<br/>
![](https://github.com/rbrianshutt/nessus/blob/main/images/nessus_with_credentials_scan.PNG)
<br />
<br />
<b>An old version of Firefox was installed.</b>   
<b>Performed another scan resulting in many vulnerabilities, particularly more Critical and High vulnerabilities. </b>
<br/>

![](https://github.com/rbrianshutt/nessus/blob/main/images/nessus_credentials%26oldfirefox.PNG)
<br />
<br />
<b>Examine vulnerabilites:</b> 
<br/>

![](https://github.com/rbrianshutt/nessus/blob/main/images/nessus_credentials_vulnerabilities.PNG)
<br />
<br />
<b>Nessus offers high level remediations for vulnerabilites.  It is suggesting I update to a current version of Firefox. </b>  
<br/>
![](https://github.com/rbrianshutt/nessus/blob/main/images/nessus_remediations.PNG)
<br />
<br />
<b>Uninstall the deprecated Firefox browser</b>
<b>Check for and install any updates in Windows.</b>
<br/>

![](https://github.com/rbrianshutt/nessus/blob/main/images/vm_windows_update.PNG)
<br />
<br />
<b>Perform scan after performing remediations.  The result is fewer vulnerabilities.</b>
<br/>

![](https://github.com/rbrianshutt/nessus/blob/main/images/nessus.scan_after_updates.PNG)

<b>Whenever possible automate updates to remediate and reduce vulnerabilites.</b>
