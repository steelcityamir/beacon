# Beacon

**Lightweight macOS agent to report system & hardware info as JSON to a central server**

## Overview

**Beacon** is a minimal, open-source macOS agent that collects system information — including macOS version, hardware model, serial number, CPU type, and RAM — and sends it as a **JSON payload** to a central API server. Designed for lightweight fleet monitoring, Beacon allows administrators or hobbyists to keep track of multiple Macs in real time.

This project also includes a minimal Go server to receive and store reports.

---

## Features

- Collect macOS version, hardware specs, and RAM/CPU info
- Produce structured **JSON payloads** for easy ingestion
- Send reports securely over HTTPS to your API server
- Can run as a CLI tool or background daemon via `launchd`
- Minimal dependencies; fully written in Swift

---

## JSON Payload Format

Beacon produces a JSON object with the following fields:

```json
{
  "osVersion": "macOS 14.6.1",
  "model": "MacBookPro18,3",
  "serial": "C02XXXXXQ05",
  "cpu": "CPU Type: 16777223",
  "ramGB": 16
}
