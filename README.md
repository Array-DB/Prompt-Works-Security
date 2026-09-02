# Prompt-Works Security

Prompt-Works Security is a security-focused fork and distribution of the OnlyKey desktop application for Arch Linux and Manjaro.

Current packaged release:

`OnlyKey-Prompt-Works-Security-Details-5.5.0.pw5-1-x86_64.pkg.tar.zst`

> This project is an independent development fork and is not an official CryptoTrust/OnlyKey release.

## Features

Prompt-Works Security keeps the existing OnlyKey workflow while adding application-side security hardening and a redesigned user experience.

- Sensitive values masked by default
- Copy passwords without displaying them
- Cryptographically secure password generator
- Removal of plaintext secret logging from the slot configuration flow
- Application integrity information
- Compact, resizable Security Details panel
- Confirmation interlock before slot writes
- Firmware Installation Wizard
- Local SHA-256 calculation for selected firmware
- Capability-based A1 authorization status
- Updated Prompt-Works interface and application icon
- Side-by-side installation with the official OnlyKey application

## A1 Touch Authorization

The desktop application alone cannot securely enforce physical A1 touch authorization.

True A1 authorization must be implemented and enforced by compatible firmware running on the OnlyKey itself.

Prompt-Works therefore does **not** claim hardware-enforced A1 authorization unless compatible firmware actually reports that capability.

## Firmware Installation Wizard

The Firmware tab provides a guided workflow:

1. Select firmware.
2. Calculate its SHA-256 locally.
3. Inspect firmware capability information.
4. Pass the firmware to the existing OnlyKey loading mechanism.
5. Leave final firmware validation to the OnlyKey device.

The wizard does **not** bypass OnlyKey firmware validation or make unsigned firmware trusted.

## Arch Linux / Manjaro Installation

Install the downloaded package with:

```bash
sudo pacman -U ~/Downloads/OnlyKey-Prompt-Works-Security-Details-5.5.0.pw5-1-x86_64.pkg.tar.zst

## SHA-256

`OnlyKey-Prompt-Works-Security-Details-5.5.0.pw5-1-x86_64.pkg.tar.zst`

```text
f381cfbe350c3d6b4fe7250efd40d8b88300b7e4cc4b2cc1458ee38a279a23d0


Verify after downloading:
sha256sum OnlyKey-Prompt-Works-Security-Details-5.5.0.pw5-1-x86_64.pkg.tar.zst


The verified SHA-256 is:
**`f381cfbe350c3d6b4fe7250efd40d8b88300b7e4cc4b2cc1458ee38a279a23d0`**.
