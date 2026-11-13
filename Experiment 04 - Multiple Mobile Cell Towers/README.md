# Experiment 04: Multiple Mobile Cell Towers

Open [Multiple Mobile Cell Towers.pkt](Multiple%20Mobile%20Cell%20Towers.pkt) in Cisco Packet Tracer 9.0.

## What it demonstrates

Four smartphones and a tablet use cellular radio links to reach a shared network. The lab shows how clients can get IP addresses from one central office and exchange traffic even when they are associated with different towers.

## What is configured

The **Kurla**, **Thane**, and **Nerul** cell towers each have a direct coaxial link to **Central Office Server0**. The server's cell tower interface is `192.168.1.1/24`. Its DHCP pool offers 50 addresses, from `192.168.1.10` through `192.168.1.59`. The phones and tablet use the `ptcellular` provider and the **3G/4G Cell1** interface.

## How to run it

1. Open the file in **Realtime** and wait for the dashed cellular links to appear. The **Fast Forward Time** button can speed up startup.
2. Open **Tablet PC0 > Config > 3G/4G Cell1**. Check for a `192.168.1.x` address. If it is blank, click **DHCP Refresh** and wait for the lease. The same check works on the smartphones.
3. Select **Add Simple PDU** (the closed envelope on the toolbar). Click **Tablet PC0** first and **Smartphone0** second. In the PDU list, look for **Successful** on the new ICMP row.
4. Switch to **Simulation**, then use **Auto Capture/Play** or **Capture/Forward** to follow the packet. Compare the event list with the dashed links on the canvas to identify which towers the devices are using. Associations can change when the topology reloads.

The tablet received a DHCP lease, and the tablet-to-phone ICMP test passed again after reopening the saved file. This file uses the simulator's combined 3G/4G mode for the handout's phone and tablet test; it does not demonstrate a 5G client connection.
