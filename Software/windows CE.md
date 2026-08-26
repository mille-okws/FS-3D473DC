# Windows CE 6.0

> **Status: Draft / Work in Progress**

The Foston FS-3D473DC runs **Microsoft Windows Embedded CE 6.0**, an embedded operating system designed for resource-constrained devices such as GPS navigation systems, industrial equipment, handheld devices, and other embedded hardware.

This document contains my notes and findings about the Windows CE environment running on the Foston.

## Device Environment

**Device:** Foston FS-3D473DC
**Operating System:** Windows CE 6.0
**Platform:** Embedded device
**CPU/SoC:** MStar — *exact model to be identified*

> ⚠️ Some information in this document is still unverified.

## Filesystem

The Windows CE filesystem contains the operating system files, applications, configuration files, and data used by the GPS.

Further investigation is required to determine:

* Which directories belong to the operating system
* Where applications are stored
* Where the GPS software is located
* How the system launches the navigation application
* Which files are persistent after reboot
* Whether additional software can be permanently installed

### Filesystem Map

```text
\
├── Windows/
│   ├── Desktop/
│   ├── Favorites/
│   ├── Fonts/
│   ├── Programs/
│   │   ├── File Viewers/
│   │   │   ├── JETCET PDF Viewer
│   │   │   ├── Office 2003 Excel Viewer
│   │   │   ├── Office 2003 PowerPoint Viewer
│   │   │   └── Office 2003 Word Viewer
│   │   ├── Media Player/
│   │   └── Windows Explorer/
│   ├── Recent/
│   └── StartUp/
│
├── appUpdate
├── BacklightCTL BMQ
├── BSPCodebase
├── BSPVersion
├── btsecurity
│
├── calibrui_0401
├── calibrui_0402
├── calibrui_0404
├── calibrui_0405
├── calibrui_0406
├── calibrui_0407
├── calibrui_0408
├── calibrui_0409
├── calibrui_040b
├── calibrui_040c
├── calibrui_040d
├── calibrui_040e
├── calibrui_0410
├── calibrui_0411
├── calibrui_0412
├── calibrui_0413
├── calibrui_0414
├── calibrui_0415
├── calibrui_0416
├── calibrui_0418
├── calibrui_0419
├── calibrui_041b
├── calibrui_041d
├── calibrui_041e
├── calibrui_041f
├── calibrui_0424
├── calibrui_0425
├── calibrui_0427
├── calibrui_0804
├── calibrui_0813
├── calibrui_081a
├── calibrui_0C0A
│
├── ceconfig
├── CheckNaNDFlashType
├── chimes
├── click
├── docviewer
├── EARTH_M
├── Exit
├── FmtTest
├── godspeed
├── GodSpeed (shortcut)
├── IAU1980
├── Identity-H
├── Identity-V
├── iesample
├── KillProc
├── loader
├── LogOutput
├── MOON
├── mt6612
├── mt6612_E2
├── Octopus
├── pdfviewer
│
└── ...
```

*This section will be expanded as the filesystem is mapped.*

## Executables

Windows CE applications generally use the `.exe` format, but executables are not necessarily compatible with desktop versions of Windows.

One of the goals of this project is to determine:

* Which executable architectures are supported
* Which Windows CE APIs are available
* Which existing applications can be executed
* How to compile custom applications for this device

## Development

One of the long-term goals is to compile and execute a custom Windows CE application directly on the Foston.

Current questions include:

* Which CPU architecture does the device use?
* Which Windows CE SDK is required?
* Which compiler/toolchain can target the device?
* Can modern toolchains be used?
* Is the original device SDK available?
* Which Win32/WinCE APIs are exposed?
* What runtime libraries are available?

This section will be updated as the development environment is investigated.

## Reverse Engineering

The Windows CE environment is being investigated alongside the physical hardware.

Relevant areas include:

* UART interfaces
* Boot process
* Filesystem
* Registry
* Executables
* DLLs
* Startup applications
* Hardware-specific drivers
* GPS software

The goal is not only to run additional software, but to understand how the original system was assembled.

## Findings

| Feature              | Status                 |
| -------------------- | ---------------------- |
| Windows CE 6.0       | ✅ Confirmed            |
| Microsoft Excel reader      | ✅ Found                |
| Microsoft PowerPoint reader | ✅ Found                |
| Paint                | ✅ Found                |
| Custom application   | 🧪 Not yet tested      |
| CPU model            | ❓ To be identified     |
| Windows CE SDK       | ❓ To be identified     |
| Boot process         | 🧪 Under investigation |

## Notes

This documentation describes observations made on a specific Foston FS-3D473DC unit.

Different hardware revisions or firmware versions may behave differently.

**Nothing here should be considered confirmed unless explicitly marked as such.**
