Stage 1 - Network Setup

In this stage the client has requested a LAN, Guest, and a DMZ network.
Our group will build this network on a FortiNet Firewall

Stage Overview:
  1. Add new devices to the workspace and link them up
  2. Configure the LAN network on the firewall through the CLI over the console interface
  3. Add a Win10 workstation to the LAN network
  4. Connect to the firewall GUI from the Win10 workstation
  5. Complete the network setup through the firewall GUI
<br>
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 1. Add new devices to the workspace and link them up
<br>

Lab Workspace:
Starting with a Pre-configured WAN-CLOUD and WAN-SWITCH

![U0aZmmS](https://github.com/spedro532/Network-Lab/assets/103095181/096cd469-3686-4071-b08c-43c8d14b4880)



<br> 
We then added a FortiNet Firewall, two Ethernet switches, and a Win10 workstation to the lab and made the following changes:

  1. Linked the WAN port on the firewall to the WAN-SWITCH
  2. Linked the LAN port on the firewall to the LAN-SWITCH
  3. Linked the DMZ port on the firewall to the DMZ-SWITCH
  4. Linked the Win10 workstation to the LAN-SWITCH

![image](https://github.com/spedro532/Network-Lab/assets/103095181/40584698-74f5-43c0-9157-f218e7629a67)

<br>
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 2. Configure the LAN network on the firewall through the CLI over the console interface

<br>

Because we are in a virtual enviorment we have to manually configer the firewall using the CLI
Per the clients request, 

We configured 10.128.0.0/24 as the LAN network.

Defined the LAN gateway as 10.128.0.1/24

Named the LAN interface Port2 on the FortiGate firewall

![image](https://github.com/spedro532/Network-Lab/assets/103095181/5489b181-6ffe-481a-9a6f-843f228fbae2)

Verified the configuration is correct

![image](https://github.com/spedro532/Network-Lab/assets/103095181/a879a32c-e69a-4208-a0ca-74caca1edba1)

<br>

Then configured the DHCP server for the LAN interface

![image](https://github.com/spedro532/Network-Lab/assets/103095181/22cb4166-7ac8-45b7-8331-74bccb884b0f)

and then verified the DHCP setup is correct

![image](https://github.com/spedro532/Network-Lab/assets/103095181/ffae466d-6055-4596-892e-a154f300f132)

<br>
--------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 3. Add a Win10 workstation to the LAN network
