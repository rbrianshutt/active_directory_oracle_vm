<h1>Home Lab Active Directory Using Oracle Virtual Box</h1>

![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/active_directory_diagram.jpg)

<h2>Description</h2>
x  
<br />


<h2>Technology Used</h2>

- <b>Oracle Virtual Box</b>
- <b>Windows 10 ISO</b>
- <b>Windows 2019 Server</b>

 
<h2>Program walk-through:</h2>


- <b>Download and install Oracle VirtualBox from the official website.</b>
- <b>Download the Windows 10 and Server 2019 ISO files.</b>

<br/>
<b>Create a new virtual machine named DC (Domain Controller) using Windows 2019 Server iso file.</b>

<br/>
<br/>
 
![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/set_up_virtualbox.PNG)
<br />
<br />
<b>Configure two network adaptors: one for a NAT internet conneciton and the other Internal for a private network.
 </b>
<br/>

![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/DC_adapter1_NAT.PNG)
![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/DC_adapter2_internal.PNG)
<br />
<br />
<b>Install Server 2019 on the virtual machine and assign IP addressing for the internal network.</b>  
<br/>
![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/ip_address_internal.PNG)
<br />
<br />
<b>Name the server and install Active Directory to create the domain.</b> 
<b>Configure routing so that clients on the private network can access the internet through the domain controller.</b>  
<br/>
![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/routing_and_remote_access.PNG)
<br />
<br />
<b>Set up DHCP on the domain controller to automatically assign IP addresses to Windows 10 machines.</b> 
<b>Range 172.16.0.100 - 172.16.0.200</b>
<br/>

![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/add_dhcp_server.PNG)
![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/dhcp.PNG)
<br />
<br />
<b>Run the PowerShell script to create 1000 users in Active Directory.</b> 
[Create Accounts Script by Josh Madakor](https://github.com/joshmadakor1/AD_PS)
<br/>
![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/powershell_create_users2.PNG)
![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/AD_users_and_computers.PNG)
<br />
<br />
<b>Create another virtual machine, install Windows 10, connect it to the private VirtualBox network, name it “Client1” and join it to the domain.
</b>  
<br/>
![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/client1_vm_internal_network.PNG)
<br />
<br />
<b>Log into the Windows 10 machine using one of the domain accounts.</b>   
<br/>

![](https://github.com/rbrianshutt/active_directory_oracle_vm/blob/main/Active%20Directory/vm_client1.PNG)
<br />
<br />
