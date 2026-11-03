# Validation and limitations

## Observations from coursework

- A legacy x86 CentOS environment was booted using UTM/QEMU on Apple Silicon.
- SSH access and legacy GCC/GDB availability were checked.
- A Fedora environment for Heartbleed-related coursework was configured and investigated through serial console and SSH.
- Some memory addresses differed from reference outputs, as expected across environments.
- The environment/approach was shared with one fellow student who encountered compatibility problems.

## Important limits

- This repository does not claim all coursework was validated by an independent reviewer.
- It does not establish that the original course VM images or files may be redistributed.
- No exact exploit walkthrough, assignment answer, or vulnerable VM image is published here.
- A future improvement would be to validate a clean-room setup using independently distributable guest images and record sanitized screenshots and reproducibility checks.

## Research relevance

The experience motivated interest in OS behavior, security boundaries, and reproducibility in systems security. It is **not** presented as original macOS IPC vulnerability research.
