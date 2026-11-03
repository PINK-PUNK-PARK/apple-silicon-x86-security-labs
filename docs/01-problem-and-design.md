# Problem and design decisions

## Problem

Legacy x86 guest systems provided for security coursework are not directly compatible with ARM-only virtualization on Apple Silicon. The original exercises assumed an x86 environment.

## Options investigated

- **ARM virtualization:** Efficient for ARM guests, but does not directly execute an x86 guest image.
- **Containers:** Useful for reproducing some web-security exercises, but a modern container does not necessarily reproduce an older guest's OS, libraries, or intentionally vulnerable software.
- **UTM/QEMU x86 emulation:** Chosen for compatibility with legacy guest architectures, accepting reduced performance relative to native virtualization.

## Engineering approach

The objective was to reproduce the essential behavior needed to study security concepts, rather than to force byte-for-byte identical outputs across different host and guest configurations.

## Scope

The work focused on guest boot, tool availability, networking, and debugging access. It did not involve modifying the macOS kernel or developing a new emulator.
