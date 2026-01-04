Wireless-Network-Auditing
Wireless Network Auditing tasks for sniffing, deauthentication attacks and capturing network packets.

Learn how to find concealed Wi-Fi networks with Python and Scapy. This tutorial aims to dismantle the security myth that surrounds hidden SSIDs and will show you how to set up your adapter in monitor mode to find and record these networks, with an emphasis on practical network analysis and security assessment techniques.

Certain network administrators mistakenly think that activating the "Hidden SSID" function completely shields their network from wardrivers or hackers. A "wardriver" is a person who "wardrives," meaning they drive around in a car using a Wi-Fi-enabled device, such as a laptop or phone, to locate and potentially exploit Wi-Fi networks. Wardriving isn't always malicious. This can be done for multiple reasons, such as finding Wi-Fi locations, doing security checks, or for fun.

This misunderstanding comes from thinking the network vanishes when the SSID isn't broadcast in Beacon frames. 

What are Beacon Frames?
Beacon frames are a category of management frames used in IEEE 802.11 WLANs. It holds details about the network. Beacon frames are transmitted periodically. They are used to indicate the presence of a wireless LAN and also to give a timing signal to synchronize communications with the devices connected to the network, which are part of a service set. Beacon frames are sent by the access point in a BSS (basic service set).

Actually, a hidden SSID network isn't truly private; just the SSID stays hidden in the Beacon frames.
Even though the SSID is hidden, it's not completely invisible because it's still sent out through certain Wi-Fi management frames, like probe requests and responses, as well as association requests. A skilled attacker might wait for a connection from a client, or they could try to disconnect the client by sending a fake deauthentication message. Once reconnected, the client will display the SSID in a minimum of one of these management frames.

This script, written in Python, is designed to capture and log Wi-Fi packets, specifically looking for and recording any SSIDs it finds. The information highlights how insecure networks are when they depend only on hidden SSIDs for protection.

A wireless adapter with monitor mode capability is necessary to find hidden SSIDs. A wireless adapter is a piece of hardware that allows a computer to join and interact with wireless networks. Within this scenario, it gathers and examines Wi-Fi packets to analyze the network. A wireless adapter is essential for capturing and processing Wi-Fi packets, and also for extracting SSID information. You will need one to run this exercise correctly. 
