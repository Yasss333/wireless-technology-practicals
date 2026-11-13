# Experiment 07: Day and Night Smart Home Automation

Open [Day and Night Smart Home Automation.pkt](Day%20and%20Night%20Smart%20Home%20Automation.pkt) in Cisco Packet Tracer 9.0.

## What it demonstrates

A door lock acts as a mode switch for a smart home. The exercise shows how one device state can drive several appliances over Wi-Fi through a central controller. “Daytime” and “Nighttime” are names for the two modes; the simulation uses the lock state as the trigger.

## What is configured

The tablet, door, ceiling fan, light, and window join the open `HomeGateway` Wi-Fi network and use DHCP. The four appliances are registered to the Home Gateway at `192.168.25.1`. Two enabled conditions on the gateway set the appliance states:

| Door lock | Mode | Window | Ceiling fan | Light |
| --- | --- | --- | --- | --- |
| Unlocked | Daytime | Open (`On = true`) | High | Off |
| Locked | Nighttime | Closed (`On = false`) | Off | On |

## How to run it

1. Leave Packet Tracer in **Realtime** and wait for the wireless links to appear.
2. Open **Tablet PC0 > Desktop > IoT Monitor**. Log in to `192.168.25.1` with `admin` / `admin`, the simulated gateway defaults.
3. Expand the four entries under **Home**. On the **Door** row, use **Lock** to trigger Nighttime. Check the window closes, the fan turns off, and the light switches on.
4. Use **Unlock** on the door to trigger Daytime. Check that the window opens, the fan goes to High, and the light turns off. The separate **Open** indicator on the door is not the trigger.
5. Open **Conditions** to see how each rule maps one door state to three appliance actions.

Both transitions were verified in IoT Monitor with all four appliances online.
