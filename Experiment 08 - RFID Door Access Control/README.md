# Experiment 08: RFID Door Access Control

Open [RFID Door Access Control.pkt](RFID%20Door%20Access%20Control.pkt) in Cisco Packet Tracer 9.0.

## What it demonstrates

The RFID reader detects a nearby card without a cable to the card. It sends the card ID to an IoT registration server, where rules decide whether to unlock the door. This demonstrates the difference between reading an identifier and authorizing access.

## What is configured

A 2960 switch connects the 2911 router, registration server, door, and RFID reader over Ethernet. The router's IOS hostname is `R1`; its `GigabitEthernet0/0` is `192.168.1.1/24`. The router's `iot` DHCP pool serves the door and reader and excludes the router and static server addresses. The server is `192.168.1.15/24` with gateway `192.168.1.1`. The door uses a copper FastEthernet adapter. Both the door and reader register with the server.

The server marks card ID `1001` as **Valid** and other IDs as **Invalid**. A valid reader state unlocks the door; a non-valid state locks it.

## How to run it

1. Leave the topology in **Realtime** and wait for the Ethernet links to turn green.
2. Drag **RFID Card** onto **RFID Reader**. The saved card is `1001`; the reader and door indicators turn green as the lock releases.
3. Drag the card away using the exposed edge of its icon. Open the card, choose **Attributes**, double-click the value for **CardID** under **Properties**, enter `500`, and press **Enter**. Close the card window and drag it onto the reader again. The reader and door indicators turn red and the door locks.
4. To inspect the rules, open **Server0 > Desktop > Web Browser** and go to `http://192.168.1.15` inside Packet Tracer. Sign in with the simulation-only credentials `rfidlab` / `rfidlab`, then select **Conditions**.

Both card IDs were tested against the reader and the corresponding door lock state was observed. The lab controls the lock; it does not swing the door open automatically.


To demonstrate it in your practical exam:

1. Open your saved **RFID Door Access Control.pkt** file and keep **Realtime** mode selected.

2. Explain the devices:
   - **R1:** provides DHCP addresses.
   - **Switch:** connects the network.
   - **Server0:** stores the IoT devices and automation rules.
   - **IoT2:** RFID reader.
   - **IoT0:** door.
   - **IoT1:** RFID card.

3. Show the rules:  
   **Server0 → Desktop → Web Browser → `http://192.168.1.15`**  
   Log in with **admin / admin**, open **Conditions**, and show all four rules enabled.

4. **Demonstrate an invalid card:**
   - Open **IoT1 → Attributes**.
   - Double-click the **CardID** value, enter **500**, and press **Enter**.
   - Close the device window.
   - Drag the card away from the reader, then back beside it.
   - Wait briefly: the reader indicates invalid and the door stays **locked (red)**.

5. **Demonstrate a valid card:**
   - Change **CardID** to **1001**.
   - Drag the card away and back beside the reader.
   - Wait briefly: the reader indicates valid and the door becomes **unlocked (green)**.

Say: **“The reader sends the card ID to the registration server. The server validates it using conditions. ID 1001 unlocks the door; any other ID locks it.”**

The door may remain visually closed when unlocked—**watch the lock indicator**.
