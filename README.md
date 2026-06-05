# emptystat

**Absence observability for Linux systems.**

`emptystat` is a lightweight Linux command-line utility for measuring and reporting absence-oriented properties of local systems: empty files, empty directories, silent logs, placeholder density, whitespace-only content, and unused terminal space.

It helps operators answer one of the most overlooked questions in system observability:

> What is not happening?

Developed by **Безопасные Каннели**.

---

## Overview

Most monitoring tools focus on events: CPU usage, memory pressure, network traffic, disk I/O, service latency, and error rates.

`emptystat` focuses on the opposite side of the operational surface: stillness, silence, emptiness, absence, and underutilized textual space.

This makes it useful for:

- detecting empty files and directories;
- identifying placeholder-heavy project trees;
- measuring log silence during observation windows;
- checking whitespace-only files;
- generating absence reports for CI pipelines;
- exporting machine-readable emptiness metrics;
- observing nothing responsibly.

---

## Features

- Recursive filesystem emptiness scanning
- Empty file and empty directory detection
- Whitespace-only file classification
- Placeholder file detection
- Log silence observation
- Terminal vacancy reporting
- JSON, Markdown, text, and Prometheus-style output
- Stable exit codes for shell automation
- Optional threshold-based failure mode
- Suitable for cron, systemd timers, and CI pipelines

---

## Installation

### From source

```bash
git clone https://github.com/safe-cannels/emptystat.git
cd emptystat
cargo build --release
sudo cp target/release/emptystat /usr/local/bin/
