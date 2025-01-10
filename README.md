<h1>Setting up Windows Active Directory</h1>

<h2>Overview</h2>
Setting up Active Directory on Windows Server 2019 involves installing the Active Directory Domain Services role, promoting the server to a domain controller, and configuring key components such as the domain, DNS settings, and DHCP. Additionally, it includes creating and managing users and computers within the domain, assigning appropriate permissions, and enabling remote access to allow for secure management and connectivity across the network.
<br />


<h2>Features Used</h2>

- <b>Active Directory Domain Services</b>
- <b>DNS</b>
- <b>Remote Access</b>
- <b>DHCP</b>
- <b>Users and Computers</b>


<h2>Lab walk-through:</h2>

<p align="center">
Select "Add roles and features".<br/>
<img src="https://i.imgur.com/2Pc7y6t.png" height="60%" width="60%"/>
<br />
<br />
Click next on the "Before you begin" screen.<br/>
Select "Role-based or feature-based installation" for the installation type and click next.<br/>
Select "Select a server from teh server pool" for the destination server, select the domain controller and click next.<br/>
<img src="https://i.imgur.com/Nph9Stw.png" height="60%" width="60%"/>
<br />
<br />
Click on Active Directory Domain Services.<br/>
<img src="https://i.imgur.com/IkXi0LI.png" height="60%" width="60%"/>
<br />
<br />
Select add features. Then click next.<br/>
<img src="https://i.imgur.com/lciHHnn.png" height="60%" width="60%"/>
<br />
<br />
Select next on the "Select features" screen.<br/>
Select next on the "Active Directory Domain Services" screen.<br/>
Select install on the "Confirm installation selections" screen.<br/>
Select close when the installation is complete.<br/>
<img src="https://i.imgur.com/sTBb4By.png" height="60%" width="60%"/>
<br />
<br />
Select the notification botton at the top right. Then select "Promote this server to a domain controller.<br/>
<img src="https://i.imgur.com/CHhAeoQ.png" height="60%" width="60%"/>
<br />
<br />
Select "Add a new forest", then enter a root domain name and click next.<br/>
<img src="https://i.imgur.com/crqbgEU.png" height="60%" width="60%"/>
<br />
<br />
On the " Domain Controller Options" screen, enter a DSRM password then click next.<br/>
Select next on the "DNS Options" screen.<br/>
Select next on the "Additional Options" screen.<br/>
Select next on the "Paths" screen.<br/>
Select next on the "Review Options" screen. Then click install.<br/>
<img src="https://i.imgur.com/OibFrK2.png" height="60%" width="60%"/>
<br />
<br />
Once the machine has restarted select "Add roles and features".<br/>
Click next on the "Before you begin" screen.<br/>
Select "Role-based or feature-based installation" for the installation type and click next.<br/>
Select "Select a server from teh server pool" for the destination server, select the domain controller and click next.<br/>
<img src="https://i.imgur.com/KN063cA.png" height="60%" width="60%"/>
<br />
<br />
Select Remote Access then click next.<br/>
<img src="https://i.imgur.com/WwqBvDs.png" height="60%" width="60%"/>
<br />
<br />
Select next on the "Select features" screen.<br/>
Select next on the "Remote Access" screen.<br/>
Click on Routing, select add features, and then click next.<br/>
<img src="https://i.imgur.com/WDuknUK.png" height="60%" width="60%"/>
<br />
<br />
Select install on the "Confirm installation selections" screen.<br/>
Select close when the installation is complete.<br/>
<img src="https://i.imgur.com/pd88zYO.png" height="60%" width="60%"/>
<br />
<br />
Click Tools at the top right then select "Routing and Remote Access".<br/>
<img src="https://i.imgur.com/YW2Q8Z8.png" height="60%" width="60%"/>
<br />
<br />
Right click on the server and select "Configure and Enable Routing and Remote Access.<br/>
<img src="https://i.imgur.com/NwXakyT.png" height="60%" width="60%"/>
<br />
<br />
Select next on the Setup Wizard.<br/>
Select Network address translation (NAT) then click next.<br/>
<img src="https://i.imgur.com/7QHF65A.png" height="60%" width="60%"/>
<br />
<br />
Select cancel on the "NAT Internet Connection" screen.<br/>
<img src="https://i.imgur.com/0jywJXD.png" height="60%" width="60%"/>
<br />
<br />
Close the Routing and Remote Access window.<br/>
Open Routing and Remote Access again by click Tools at the top right then select "Routing and Remote Access".<br/>
Right click on the server and select "Configure and Enable Routing and Remote Access.<br/>
Select next on the Setup Wizard.<br/>
Select Network address translation (NAT) then click next.<br/>
Select the NAT interface then click next.<br/>
<img src="https://i.imgur.com/GhyZ4rS.png" height="60%" width="60%"/>
<br />
<br />
Select finish to close the Setup Wizard.<br/>
Routing and Remote Access has been setup.<br/>
<img src="https://i.imgur.com/fDnDOcI.png" height="60%" width="60%"/>
<br />
<br />
Close the Routing and Remote Access window then select "Add roles and features".<br/>
Click next on the "Before you begin" screen.<br/>
Select "Role-based or feature-based installation" for the installation type and click next.<br/>
Select "Select a server from teh server pool" for the destination server, select the domain controller and click next.<br/>
Click on DHCP Server, select add features, and then click next.<br/>
<img src="https://i.imgur.com/4qASPmR.png" height="60%" width="60%"/>
<br />
<br />
Select next on the "Select features" screen.<br/>
Select next on the "DHCP Server" screen.<br/>
Select install on the "Confirm installation selections" screen.<br/>
Select close when the installation is complete.<br/>
<img src="https://i.imgur.com/9DafdXk.png" height="60%" width="60%"/>
<br />
<br />
Click Tools at the top right then select "DHCP".<br/>
Expand the DHCP server, right click on IPv4, and select new scope.<br/>
<img src="https://i.imgur.com/SfZkq3H.png" height="60%" width="60%"/>
<br />
<br />
Click next on the new scope setup wizard.<br/>
Enter a name and a description then click next.<br/>
<img src="https://i.imgur.com/VbZeeG1.png" height="60%" width="60%"/>
<br />
<br />
Enter an IP Address Range to be distributed to the client.<br/>
<img src="https://i.imgur.com/Zib95R2.png" height="60%" width="60%"/>
<br />
<br />
Click next on the "Add Exclusion and Delay" screen.<br/>
Click next on the "Lease Duration" screen.<br/>
Select "Yes, I want to configure these options now" on the "Configure DHCP Options" screen then click next.<br/>
Enter the IP address of the host(internal) network interface card as the Router (Default Gateway) then click next.<br/>
<img src="https://i.imgur.com/oLxIFM7.png" height="60%" width="60%"/>
<br />
<br />
Remove the NAT IP address and add the host(internal) IP address then click next.<br/>
<img src="https://i.imgur.com/4K4sLcQ.png" height="60%" width="60%"/>
<br />
<br />
Remove the NAT IP address then click next.<br/>
<img src="https://i.imgur.com/cAq4d7A.png" height="60%" width="60%"/>
<br />
<br />
Select "Yes, I want to activate this scope now" then click next.<br/>
Click finish to close the new scope wizard.<br/>
Right click the DHCP server then select authorize.<br/>
<img src="https://i.imgur.com/3WpnFoN.png" height="60%" width="60%"/>
<br />
<br />
Right click the DHCP server then select refresh.<br/>
The DHCP server is now active.<br/>
<img src="https://i.imgur.com/w9cYHYe.png" height="60%" width="60%"/>
<br />
<br />
Click Tools at the top right then select "Active Directory Users and Computers".<br/>
Right click on the domain name, select new, then click on Organizational Unit.<br/>
<img src="https://i.imgur.com/BFMLezT.png" height="60%" width="60%"/>
<br />
<br />
Enter a name and click ok.<br/>
<img src="https://i.imgur.com/nCH1uQY.png" height="60%" width="60%"/>
<br />
<br />
Create 2 more Organizational Units.<br/>
<img src="https://i.imgur.com/ilh4p9F.png" height="60%" width="60%"/>
<br />
<br />
Right click on the Admin Organizational unit created, select new, then click user.<br/>
<img src="https://i.imgur.com/JulkgJO.png" height="60%" width="60%"/>
<br />
<br />
Enter the user's information then click next.<br/>
<img src="https://i.imgur.com/cPSCXLh.png" height="60%" width="60%"/>
<br />
<br />
Enter a password then click next.<br/>
Click finish.<br/>
<img src="https://i.imgur.com/ZMETaiI.png" height="60%" width="60%"/>
<br />
<br />
Create 2 more users for each Organizational unit.<br/>
<img src="https://i.imgur.com/R5iFM0b.png" height="60%" width="60%"/>
<img src="https://i.imgur.com/XE7k7WC.png" height="60%" width="60%"/>
<br />
<br />
Open the Admin Organizational unit, right click on the user and select Properties.<br/>
<img src="https://i.imgur.com/ojCxERj.png" height="60%" width="60%"/>
<br />
<br />
Select "Member Of" then click add.<br/>
Enter Administrators in the text box, click check names, then click ok.<br/>
<img src="https://i.imgur.com/dnISD1c.png" height="60%" width="60%"/>
<br />
<br />
Click apply then click ok.<br/>
<img src="https://i.imgur.com/q5EymEC.png" height="60%" width="60%"/>
<br />
<br />
Sign out and sign back in with the admin account.<br/>
<img src="https://i.imgur.com/tqfHBwS.png" height="60%" width="60%"/>
<br />
<br />
Open up Command Prompt and enter "whoami" the verify the current user.<br/>
<img src="https://i.imgur.com/BoauJAe.png" height="60%" width="60%"/>
<br />
<br />
</p>

