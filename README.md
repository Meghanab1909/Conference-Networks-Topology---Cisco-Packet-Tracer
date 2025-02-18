# Files of this Repository

1. Conference Networks.pkt
2. Output Screenshots
   - output-1.png
   - output-2.png
   - output-3.png
   - output-4.png
   - output-5.png
3. Project Screen Recording.mp4: Demonstrates the working of the .pkt file. To get a better understanding of the project and its working please download the .mp4 file.

# About the topology
 <table>
   <tr>
     <td>Devices</td>
     <td>Purpose</td>
   </tr>
   <tr>
     <td>
       1 Router 
     </td>
     <td>
       Main Central Router
     </td>
   </tr>
   <tr>
     <td>
       3 Switches: 1 Core Switch and 2 Access Switches
     </td>
     <td>
       Core Switch: Contact Point for all the devices<br>
       Access Switches: Connected to Core Switch<br>
       <b>There are 10 PCs connected to each switch</b>
     </td>
   </tr>
   <tr>
     <td>Access Point</td>
     <td>
       Wireless Connection<br>
       <b>There are 20 wireless laptops connected to Access Point</b>
     </td>
   </tr>
   <tr>
     <td>
       Proxy Server
     </td>
     <td>
        HTTP and HTTPS: On<br>
        DHCP Configured
     </td>
   </tr>
   <tr>
     <td>
       ASA 5506
     </td>
     <td>
       SSL-VPN<br>
       Provides authentication and security
     </td>
   </tr>
   <tr>
     <td>PCs</td>
     <td>Client Devices (End-Devices)<br>The devices are DHCP Configured</td>
   </tr>
   <tr>
     <td>Laptops</td>
     <td>Client Devices (End-Devices)<br>The devices are DHCP Configured</td>
   </tr>
 </table>

 # How to Run
 1. Download the file and wait for the connection arrows to turn to green.
 2. Once the arrows turn green, hover over the end-devices to check if the IP Address, Default Gateway and DNS Server is set. If its not move to step 3 else move to step 4.
 3. Click on each device and reset by clicking on static and clicking on dhcp.
    <br>Note: DHCP is on a lease so if at all the device is set to DHCP and then reset, type <b>dhcp /renew</b> on command prompt to renew the DHCP configuration. Make sure the IP address gets set to an IP starting with 192.168.1 (instead of starting 169. . .)
4. Carry out packet transmission, ping to check end-to-end connectivity.
5. Before checking the vpn portal, the bookmark manager and user manager settings are as follows:
   <br>
   - Bookmark Manager Settings: <br>
      - Bookmark Title: Conference_Server
      - URL: https://192.168.1.100<br>
   - User Manager Settings:<br>
      - Username: vpnguest
      - Bookmark: Conference_Server (Selected from dropdown list)
      - Profile Name: VPNUSER
      - Group Policy: VPNGROUP
7. To check VPN, on any of the client end-device type https://192.168.1.250, the VPN portal will open after which enter <b>vpnguest (as username)</b> and <b>conf@123 (as password)</b>.
   The clientless VPN portal will open and there will be a link named <b>Conference_server</b> on clicking it, it opens up the server files (like index.html, conference_dashboard.html, image.html, helloworld.html). The index.html has a hyperlink named <b>Conference Dashboard</b> directing the users to the Conference Portal.


   


