# Experiment 02 - Bluetooth Personal Area Network

This lab shows how nearby devices discover and pair over Bluetooth and how a beacon reaches nearby receivers. The two checks illustrate the difference between a paired connection and broadcast traffic.

PC0 is paired with the IoT appliance (IoT0) and Bluetooth speaker (IoT1). Bluetooth is enabled on all three devices. The appliance broadcasts a beacon every 10 seconds.

## Run it

1. Open the .pkt in Cisco Packet Tracer 9.0. On PC0, open Desktop > Bluetooth. IoT0 and IoT1 should show **Paired, Connected**.
2. If you need to recreate the pairing, verify Bluetooth and Discoverable are on, select Discover, select each device, and click Pair. Accept the simulated pairing prompt if it appears.
3. Switch to Simulation mode and enable Bluetooth under Edit Filters. Use Capture/Forward to step through the beacon. In the event list, look for IoT0 as the sender and PC0 and IoT1 as receivers. Both received the beacon during testing.
