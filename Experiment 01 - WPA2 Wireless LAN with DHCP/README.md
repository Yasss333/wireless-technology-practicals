# Experiment 01 - WPA2 Wireless LAN with DHCP

This lab shows how a wireless router authenticates Wi-Fi clients, assigns their IP addresses, and forwards traffic between them. It separates two questions you can check independently: whether a client joined the WLAN and whether it can reach another client.

The WRT300N advertises WLAN-Network with WPA2-PSK (AES). Laptop0 and Laptop1 use WPC300N adapters, and PC0 uses a WMP300N. All three use DHCP on 192.168.0.0/24, with the router at 192.168.0.1.

## Run it

1. Open the .pkt in Cisco Packet Tracer 9.0 and select Realtime. Wait for the three dotted wireless links to appear.
2. On each client, open Desktop > IP Configuration and check that Wireless0 has a DHCP address in 192.168.0.0/24. If a client is disconnected, check its SSID and WPA2 settings under Config > Wireless0. The simulated passphrase is cisco12345.
3. Click Add Simple PDU (the closed envelope), then Laptop0 and Laptop1. Repeat with Laptop0 and PC0. Check the PDU list for **Successful**. Both pairs passed in the saved setup.
