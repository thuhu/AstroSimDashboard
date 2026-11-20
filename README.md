# AstroSimDashboard

Downloads for AstroSimDashboard, a physical dashboard for **Farming Simulator 25**
running on the **STM32H745I-DISCO** board: speed, revs, gear, fuel, lights,
attachments, grain tank and cargo, live from the game on the board's touch screen.

This repository only holds releases. Get the files from
[Releases](../../releases).

## Firmware

Each release has the board firmware in two formats; use whichever your tool prefers:

| File | Use with |
|---|---|
| `AstroSimDashboard-firmware-vX.Y.Z.hex` | STM32CubeProgrammer, most flashing tools (address included) |
| `AstroSimDashboard-firmware-vX.Y.Z.bin` | tools that need a start address: flash at **0x08000000** |

### Flashing with STM32CubeProgrammer

1. Connect the board's **ST-LINK** USB port to the PC.
2. In STM32CubeProgrammer choose **ST-LINK**, click **Connect**.
3. Open **Erasing & Programming**, pick the `.hex` file (for the `.bin`, enter start
   address `0x08000000`), tick **Verify programming**, click **Start Programming**.
4. Unplug the board and plug it back in once, so it starts at full speed (400 MHz).

## Connecting to the game

Plug the board's **user USB port** (the micro-USB next to the network jack) into the
PC; it shows up as a serial port without a driver. The board can also connect over
the network. On the PC you need the game mod and the DashBridge app.

## Licenses

The firmware includes lwIP (BSD 3-Clause), TinyUSB (MIT) and the Barlow fonts
(SIL Open Font License 1.1).
