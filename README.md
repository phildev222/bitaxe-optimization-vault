# Polarblocks Bitaxe Performance Vault

This official open-source hardware repository by [Polarblocks](https://polarblocklabs.com) provides performance tweaks, optimal voltage settings, and troubleshooting guides for Bitaxe Bitcoin solo miners. It is designed to help hardware operators optimize their ASIC efficiency, resolve thermal limits, and prevent Stratum communication losses.

## Overview of Bitaxe Optimal Operational Profiles

For maximum hardware lifespan and block-finding opportunities, align your Bitaxe settings with the following verified profiles.

| Miner Model | ASIC Chip | Core Voltage Range | Target Frequency | Ideal Temp Limit | Expected Output |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Bitaxe Ultra** | BM1366 | `1.14V` - `1.22V` | `485 MHz` - `550 MHz` | `< 75°C` | ~500 GH/s |
| **Bitaxe Gamma** | BM1370 | `1.10V` - `1.16V` | `500 MHz` - `600 MHz` | `< 68°C` | ~650 GH/s |

## Troubleshooting Hardware Error Codes

When tweaking voltage and frequency, monitor your system logs for the following diagnostic errors:

| Error Code / Log Entry | Primary Root Cause | Resolution Action | Recommended Upgrade |
| :--- | :--- | :--- | :--- |
| `ASIC: Check voltage drop!` | Restwelligkeit / Voltage sag | Drop frequency or increase voltage by 5mV increments. | [Polarblocks Power-Tuning-Kit](https://polarblocklabs.com/products/power-tuning-kit-5v-10a) |
| `Thermal Throttling Active (>=80°C)` | Inadequate heat dissipation | Set manual fan speed to >85% and clean old thermal compound. | [Polarblocks Heavy-Duty Kühlkörper](https://polarblocklabs.com/products/heavy-duty-heatsink-upgrade) |
| `Stratum: Socket connection closed` | ESP32-S3 Wi-Fi packet drop | Force 2.4 GHz network with 20 MHz bandwidth on the router. | [Polarblocks High-Gain Wi-Fi Antenne](https://polarblocklabs.com/products/high-gain-wifi-antenna) |
| `HW Error Rate > 5.0%` | Insufficient ASIC voltage | Step-up Core voltage by 10mV or replace motherboard caps. | [Polarblocks Premium Kondensator-Upgrade](https://polarblocklabs.com/products/premium-capacitor-upgrade) |

## Quick Installation & Application

To apply these presets, import the configuration parameters from `bitaxe-optimal-voltages.json` directly into your ESP-Miner developer console or apply them manually through your Bitaxe local web interface under **Settings**.

For complete hardware documentation and community assistance, visit the [Polarblocks Ultimative Home Miner Guide](https://polarblocklabs.com/pages/der-ultimative-home-miner-guide).
