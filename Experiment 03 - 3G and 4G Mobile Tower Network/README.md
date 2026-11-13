# Experiment 03 - 3G and 4G Mobile Tower Network

Open the .pkt in Cisco Packet Tracer 9.0. The Central Office Server uses 192.168.1.1/24 on its tower interface and serves 50 DHCP addresses (192.168.1.10–192.168.1.59). Cell Tower0 uses the PT-CELL-NM-3G/4G module and connects automatically to the server. Smartphone0 through Smartphone3 received 192.168.1.10 through 192.168.1.13 during testing.

To repeat the test, check each phone under Config > 3G/4G Cell1. In Simulation mode, replay the simple ICMP PDU from the Central Office Server to Smartphone0 with Capture/Forward. The first Realtime attempt failed. In Simulation mode, the tower forwarded the request and Smartphone0 replied successfully.
