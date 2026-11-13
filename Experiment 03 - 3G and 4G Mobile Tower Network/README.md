# Experiment 03 - 3G and 4G Mobile Tower Network

This lab shows how four smartphones use a cell tower to reach a Central Office Server. The DHCP check verifies addressing, and the ICMP trace shows how the tower carries a request and reply.

Cell Tower0 uses the PT-CELL-NM-3G/4G module and links automatically to the Central Office Server. The server uses 192.168.1.1/24 on its Cell Tower interface. Its DHCP pool provides 50 addresses from 192.168.1.10 through 192.168.1.59.

## Run it

1. Open the .pkt in Cisco Packet Tracer 9.0. Check for a link from the server to the tower and four cellular links from the tower to the phones.
2. On each phone, open Config > 3G/4G Cell1. Use DHCP Refresh if needed and wait for the IPv4 address. Smartphone0 through Smartphone3 received 192.168.1.10 through 192.168.1.13 during testing.
3. Switch to Simulation mode. Replay the saved ICMP PDU, or click Add Simple PDU, then the Central Office Server and Smartphone0. Use Capture/Forward to follow the request and reply through the tower. The first Realtime attempt failed, and the stepped Simulation test showed **Successful**.
