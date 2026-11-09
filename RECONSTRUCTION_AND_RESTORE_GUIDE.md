# RECONSTRUCTION AND RESTORE GUIDE: social-benchmark (Standalone Pre-Partition Benchmark)
**Generated At:** 2026-10-30 11:56:41  
**Origin Path:** `D:\social-benchmark`  
**Primary Branch:** `main`  
**HEAD Commit at Backup:** `3760e083e513c2d2fe9283751ecca67bc6e0b336`  
**Tracked Files in Archive:** 24  
**Remote Repository:** `Local Standalone (No Remote)`  

---

## 1. System Overview & Architecture
* **Role:** Pre-partition standalone implementation of the social benchmark harness
* **Available Branches:** * main
* **Language & Runtime:** Rust Edition 2024 / LLVM / Tokio Async Runtime
* **Storage & Memory Model:** Memory-Mapped B+Tree (LMDB / heed) + 4KB Page-Aligned Direct I/O WAL (`write-harness`)

---

## 2. Restoration & Extraction Instructions

This archive contains the **entire source tree** and the **complete `.git` metadata directory** (branches, tags, reflogs, and commit history).

### Step 1: Decompress Archive
Extract this `.zip` archive to any target destination directory:
```powershell
Expand-Archive -Path "social_benchmark_backup.zip" -DestinationPath "D:\restored\social-benchmark-legacy"
cd "D:\restored\social-benchmark-legacy"
```

### Step 2: Verify Git Repository Integrity
Once extracted, git is immediately fully functional with zero initialization steps required:
```powershell
git status
git log --oneline -n 10
git branch -a
git checkout main
```
Verify that `git rev-parse HEAD` outputs `3760e083e513c2d2fe9283751ecca67bc6e0b336`.

---

## 3. Build & Compilation Verification

### Prerequisites
* Rust toolchain (1.85+ / 2024 edition): `rustup default stable`
* C Compiler / Linker for Windows (`x86_64-pc-windows-gnu` or MSVC) / Linux (`gcc` / `clang`)

### Build Commands
```powershell
# Build optimized release binaries
cargo build --release

# Execute full verification test suite
cargo test --release
```

---

## 4. Remote Synchronization (If applicable)
To synchronize with the upstream GitHub repository:
```powershell
# Local repository - no remote upstream configured.

```

---
*Archival standard: SHA-256 integrity verification, 100% commit graph fidelity, zero data loss.*
