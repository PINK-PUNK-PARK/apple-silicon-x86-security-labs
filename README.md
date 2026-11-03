# Reproducing Legacy x86 Security Labs on Apple Silicon

A student-authored engineering case study about running legacy x86 security lab environments on an Apple Silicon Mac using UTM/QEMU.

> **Scope:** Documentation of environment setup and troubleshooting only. This repository does **not** redistribute course materials, VM images, assignment instructions, exploit code, or completed assignment solutions.

## Motivation

Some students using Apple Silicon Macs encountered architecture-compatibility challenges with older x86 virtual machines used in security coursework. I explored a reproducible emulation-based setup and shared my approach with one classmate experiencing similar issues.

## Environment

- Host: Apple Silicon MacBook Pro (M3 Pro), macOS 15
- Emulation: UTM / QEMU for x86 guests
- Guest environments explored: legacy CentOS for stack-overflow exercises and Fedora for Heartbleed-related lab setup
- Connectivity: virtual networking and SSH

## What I worked on

1. Diagnosed the difference between ARM virtualization and x86 emulation.
2. Evaluated VM and container approaches for legacy guest compatibility.
3. Configured UTM/QEMU x86 guests and virtual networking.
4. Verified guest boot, SSH access, and availability of relevant debugging/build tools.
5. Compared observable lab behavior with expected exercise requirements, noting that environment-dependent addresses can differ.

## Documentation

- [Problem and design decisions](docs/01-problem-and-design.md)
- [Environment and networking](docs/02-environment-and-networking.md)
- [Validation and limitations](docs/03-validation-and-limitations.md)

## Reproducibility and boundaries

This is a technical process log, **not** a turnkey copy of the course lab. Readers must obtain authorized guest images and assignment materials from their own instructor or other legitimate sources. Details are intentionally limited to general emulation and connectivity; screenshots and command outputs will be added only after reviewing them for academic-integrity and privacy concerns.

## Status

Documentation draft. The underlying environments were configured during coursework, but the instructions in this repository have not been independently re-run end-to-end from a clean machine.
