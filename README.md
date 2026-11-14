# NUCLEO-H723ZG 3D Explorer

An interactive 3D learning page for the **STM32 NUCLEO-H723ZG (MB1364)**. Rotate the board, hover any part to see what it does, flip it over to see the back, and read the manual’s power, jumper, solder-bridge, pinout and safety information in one place.

**Live demo:** `https://simsim-cs.github.io/nucleo-h723zg-3d-explorer/` (after you enable GitHub Pages)

## Features

- **3D board** built from the front and back board pictures. Click-drag to rotate, scroll to zoom, hover for a label, click for detail.
- **About 70 hover targets:** the MCU, ST-LINK, USB and Ethernet connectors, jumpers JP1–JP6, LEDs LD1–LD8, buttons, Zio and morpho headers, crystals, regulators, test points and solder-bridge groups on the back.
- **Show back** button to flip the board.
- **Lessons (15):** quick start, safe power-up, Zephyr blinky and console, external debugger, current measurement, 1.8 V / 3.3 V, USB OTG, Ethernet, clocks, Arduino shields, FDCAN, VBAT.
- **Connectors tab:** full pin tables for CN1, CN5, CN7–CN10, CN11/CN12, CN13, CN14.
- **Power tab:** the five supply options, JP2 positions, limits, and the safe power-up order.
- **Config tab:** default jumpers, HSE/LSE options, virtual COM port, USB and Ethernet pins, solder bridges.
- **Safety tab:** handling, powering and I/O cautions, compliance and disposal.

## Run it

It is a single static file.

```bash
git clone https://github.com/simsim-cs/nucleo-h723zg-3d-explorer
cd nucleo-h723zg-3d-explorer
python3 -m http.server 8000   # then open http://localhost:8000
```

Opening `index.html` directly from disk may block the board textures in some browsers, so use a local server or GitHub Pages. three.js (r128) loads from cdnjs.

## Sources and accuracy

- **UM2407 Rev 6** (April 2026), *STM32H7 Nucleo-144 boards (MB1364)*, for connectors, power, clocks, jumpers, solder bridges and safety.
- **Zephyr docs**, *Nucleo H723ZG*, for the default peripheral mapping and flashing.
- Part positions are placed by eye from the board pictures. A few parts are marked **inferred** (for example U11, U12, U13) because the manual doesn’t number them.
- The manual prints default solder-bridge states in bold. Check Table 14 in the PDF before cutting or bridging anything.
- This is a learning aid, not a substitute for the manual or schematic. Verify before wiring or powering real hardware.

## Credits and legal

Not affiliated with or endorsed by STMicroelectronics. STM32, Nucleo and ST are trademarks of STMicroelectronics. Board pictures and manual data belong to their owners. The code in this repo is MIT licensed, and that licence does not cover third-party images or manual content.

## Contributing

Fixes to labels or positions are welcome. Open an issue with the part ID, what’s wrong, and the page of UM2407 that backs it up.

## License

MIT, see [LICENSE](LICENSE).
