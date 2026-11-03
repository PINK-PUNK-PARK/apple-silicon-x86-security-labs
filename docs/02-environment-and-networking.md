# Environment and networking notes

## Host and guest setup

- Host: macOS 15 on Apple M3 Pro.
- Emulation: UTM backed by QEMU, configured for x86 guest execution.
- Legacy CentOS guest: booted and accessed over SSH; GCC and GDB availability checked.
- Fedora guest: serial-console and SSH troubleshooting performed for the Heartbleed-related environment.

## Networking lessons

- An emulated NIC must have a guest-compatible device model; one working configuration used `rtl8139`.
- Shared/NAT networking can change guest IP addresses; confirm the current guest address rather than assuming it remains fixed.
- SSH access requires a running guest SSH server and an appropriate virtual network route.
- A serial console can help when graphical display output stalls.

## General verification checklist

1. Confirm guest architecture and OS version.
2. Verify the guest has booted and networking is configured.
3. Confirm SSH access from the host where permitted.
4. Check required compiler/debugger and cryptographic library versions.
5. Record environmental differences before comparing lab observations.

No instructor-supplied VM images, course scripts, or assignment-specific payloads are included.
