# Project Polaris — Raydin Labs Flight Controller

> One platform. Any vehicle. Configure, don't compromise.

FCV1 is a modular, reconfigurable flight control platform designed to work 
across drones, quadplanes, tricopters, bicopters, CanSats, and rockets — 
without rebuilding from scratch for each application.

## The Problem

Every vehicle class today uses a different flight controller, a different 
firmware stack, and a different toolchain. The physics overlaps. The tooling 
doesn't. FCV1 fixes that.

## How It Works

- **Set a vehicle mode** — declare what you're building
- **The system configures itself** — control laws, sensor fusion, mixer 
  geometry, I/O mapping, and safety logic load automatically
- **Swap sensors freely** — hardware abstraction layer supports multiple 
  IMUs, barometers, and GPS modules interchangeably

## Vehicle Modes (Planned)
- [ ] Quadcopter
- [ ] Tricopter
- [ ] Bicopter  
- [ ] Quad Plane (VTOL)
- [ ] CanSat / Sounding Rocket
- [ ] CubeSat ADCS (coming later)

## Architecture
- **MCU:** STM32F405
- **AHRS:** Madgwick filter / EKF quaternion fusion
- **Control:** Cascaded PID with configurable mixer
- **Comms:** UART telemetry, ESP32 bridge for live tuning
- **PCB:** Custom hardware (EasyEDA project included)

## Status
🔧 Active development — firmware and PCB designs uploading progressively.
Follow the build journey on [YouTube](#) and [Instagram](#).

## Repository Structure (WIP)
```
FCV1/
├── firmware/        # STM32 firmware source
├── hardware/        # PCB schematics and layouts
├── docs/            # Architecture documentation
└── tools/           # Calibration and config utilities
```

## License
Apache 2.0 — open to build on, protected for commercial use.

---
Built by [Raydin Labs](https://github.com/raydinlabs) 🛸
