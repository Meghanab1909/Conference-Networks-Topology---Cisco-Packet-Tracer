# Files of this Repository

1. Conference Networks.pkt
2. Output Screenshots
   - output-1.png
   - output-2.png
   - output-3.png
   - output-4.png
   - output-5.png

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
    Note: DHCP is on a lease so if at all the device is set to DHCP and then reset, type _dhcp /renew_ on command prompt to renew the DHCP configuration.
4. Carry out packet transmission, ping to check end-to-end connectivity.
5. Before checking the vpn portal, in this topology the proxy server is dhcp configured so make sure to update the server ip in bookmark manager and user manager in ASA0 Config Tab.
   <br>
   - Bookmark Manager Settings (can be changed): <br><b>Bookmark Title: Server ; URL: https://<ip_of_proxy_server>. Click Add</b><br>
   - User Manager Settings (can be changed):<br><b>Username: <shall_be_set> (due to set VPN settings) ; Bookmark: Select _Server_ from dropdown list ; Profile Name: VPNUSER ; Group Policy: VPNGROUP</b>
7. To check VPN, on any of the client end-device type *https://192.168.1.250*, the VPN portal will open after which enter vpnguest (as username) and conf@123 (as password).
   The clientless VPN portal will open and there will be *server* link on clicking it, it opens up the server files (like index.html, image.html, helloworld.html).
   


