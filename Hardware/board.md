# Board

## Device Information

The Foston FS-3D473DC is an automotive GPS navigation device based on a **Cortex-A9 SoC** and running **Windows Embedded CE 6.0**.

The following information was obtained directly from the device:

| Parameter          | Information                |
| ------------------ | -------------------------- |
| Device             | Foston FS-3D473DC          |
| Board / Platform   | GPS4320                    |
| EVB                | Semiconductor EVB 6.0      |
| Operating System   | Windows Embedded CE 6.0    |
| CPU                | ARM Cortex-A9              |
| SoC                | MSB2531                    |
| CPU Frequency      | 800 MHz                    |
| RAM                | 128 MB                     |
| Flash Storage      | 4 GB                       |
| Display Resolution | 480 × 272 pixels           |
| Display Colors     | 65,536                     |
| ROM Version        | `84.pm.d.ne.m-5.020140926` |

## Processor

The device uses an **MStar MSB2531** SoC with an ARM Cortex-A9 CPU running at **800 MHz**.

Further investigation is required to identify the complete set of peripherals integrated into the SoC and determine which ones are used by the Foston.

## Memory

The device reports:

* **RAM:** 128 MB
* **Flash:** 4 GB

The exact memory chips and their interfaces have not yet been identified.

## Display

The Foston uses a display with:

* Resolution: **480 × 272 pixels**
* Color depth: **65,536 colors**

The display controller and exact panel model are currently unknown.

## Platform

The device identifies itself as:

```text
GPS4320
Semiconductor EVB 6.0
```

It runs:

```text
Windows Embedded CE 6.0
```

The relationship between the **GPS4320** platform identifier, the **Semiconductor EVB 6.0** designation, and the MSB2531 SoC is still being investigated.

## Current Status

| Component                   | Status                 |
| --------------------------- | ---------------------- |
| Board / Platform            | ✅ Identified           |
| SoC                         | ✅ Identified           |
| CPU architecture            | ✅ Identified           |
| CPU frequency               | ✅ Identified           |
| RAM capacity                | ✅ Identified           |
| Flash capacity              | ✅ Identified           |
| Display resolution          | ✅ Identified           |
| Display color depth         | ✅ Identified           |
| ROM version                 | ✅ Identified           |
| Exact RAM chip              | ❓ Unknown              |
| Exact Flash chip            | ❓ Unknown              |
| Display panel model         | ❓ Unknown              |
| Complete peripheral mapping | 🧪 Under investigation |
