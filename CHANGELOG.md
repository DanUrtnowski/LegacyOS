# LegacyOS — public milestone record

This file records milestones that are publicly verifiable. It is not the
development changelog; day-to-day work stays private. Only outcomes that were
actually observed are listed.

## 2026-11-02 — First verified prototype

- NetBSD 11.0 i386 installed under emulation from a hash-verified official ISO
  using a scripted, headless QEMU lab.
- Installed system booted to `login:` from disk with no install media attached.
- Interactive login, file write and orderly ACPI shutdown confirmed.
- The guest's native toolchain built the project's original C sources on-box.
- `los`, the original 80×25 text desktop, ran with overlapping windows, taskbar,
  launcher and file manager.
- `cpubench` and the deterministic workload produced a stable checksum and a
  `RESULT: PASS`.
- A Pentium III profile (`-cpu pentium3 -m 128`) reached the login prompt.

### Recorded as inconclusive, not as a result

- 486-class profile: kernel boots and attaches devices, but the capture window
  was too short to reach a conclusion. Tier A remains unproven.
- Two further profiles aborted on a dirty disk image left by an earlier forced
  stop. Those runs are recorded as invalid rather than as CPU results.

## Not yet started

Physical-hardware bring-up, a distribution image, and custom-kernel work for
low-RAM configurations.
