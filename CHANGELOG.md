# Beside for Android — Changelog

## [0.3.0] (versionCode 13) — 2026-11-12
### Added & Improved
- Independent platform release tagged as `android-v0.3.0` (versionCode 13).
- **Kernel-Level Atomic Non-Overwriting Rename**: Replaced secondary userspace data copying and double-fsync churn through Android's emulated FUSE storage (`/sdcard/Download`) with native `renameat2(..., RENAME_NOREPLACE)` syscalls.
- **Physical Device Benchmark Results**: Folder transfers with 50 small files now complete in **5.5 seconds** (down from 21.2s on v0.2.0) — a **3.85x speedup (74% latency reduction)**.
- **CPU & Thermal Efficiency**: Android CPU time dropped by ~38% during folder transfers, keeping device thermals cool (24.5°C) and conserving battery during multi-file transfers.
- **Elimination of Upload Nagle Stalls**: Enabled `TCP_NODELAY` across all sockets, delivering up to **2.63x faster** file uploads from Android to Windows PC.
- 100% SHA-256 data integrity verified across all physical runs.

## [0.2.0] (versionCode 11) — 2026-11-01
### Added & Improved
- Independent platform release cycle (tagged as `android-v0.2.0`).
- Cryptographic Ed25519 release feed signature verification.
- Android 12 through Android 16 sideloading guide and in-place upgrade preservation.
- Xiaomi MIUI / HyperOS and Samsung One UI background listening battery optimization instructions.
- Bounded 64 KB streaming over Mutual TLS 1.3 with Android Keystore AES-256-GCM.
