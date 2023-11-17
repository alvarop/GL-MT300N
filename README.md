# GL-INet - GL-MT300N Setup (WiFi to Internet)

First, connect the computer to the router's LAN port. Once connected, go to the router’s IP address. In this case 192.168.8.1.

![Opening Screen](images/image16.png)

Set a new admin password if prompted.

![Admin password selection screen](images/image2.png)

Go to the **Internet** page.

![Internet page](images/image3.png)

Scroll down to the repeater section and click on **scan**.

![Repeater Section - Scan](images/image1.png)

This will allow the router to connect to a local wifi network. Select the correct SSID and enter the password.

![WiFi - SSID/Password Selection](images/image4.png)

The Internet page should be updated to show that the router is connected to the internet over WiFi.

![Internet page showing connection](images/image6.png)

Before proceeding, you might want to click on Upgrade and make sure you have the latest router firmware.

On another window, go to \<insert final URL here, I used pop.bgpvps.com:10086\> and click on request a tunnel.

![POP Login Page](images/image5.png)

Add a tunnel name and click on the arrows on the right to generate a preshared key. You can also request to get the configuration by email.

![Request a Tunnel Page](images/image8.png)

Write down your tunnel details and make sure you save the configuration below (qg-quick) since it will be used to configure the router.

![Tunnel Details Page](images/image7.png)

Optionally, you can use the generated QR code to copy the information.

![Tunne Details QR Code](images/image11.png)

Back on the GL-iNET router, go to VPN and click on WireGuard client.

![WireGuard Client Page](images/image9.png)

Click on **Set Up WireGuard Manually** and add a name for the tunnel.

![Add a new WireGuard Client Page](images/image10.png)

Under **Configuration**, paste in the wg-quick text from before and click next.

The new tunnel should now be visible in the WireGuard Client page

![WireGuard Client Page before connection](images/image12.png)

Select the new server from the dropdown and press connect.

![WireGuard Client Page with connection information](images/image13.png)

You can now verify that your external IP address matches the tunnel.

!["What is my ip?" Google search](images/image14.png)

Traceroute can also be used to see how the traffic gets to its destination.

![Traceroute](images/image15.png)

