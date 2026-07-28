<div align="center">

# 🌐 Universal Bricked Router Recovery Guide

### Recover a soft-bricked router using the built-in **TFTP Recovery Mode**
### 🚫 No USB-to-TTL Adapter Required *(If your bootloader supports TFTP recovery)*

![GitHub Repo stars](https://img.shields.io/github/stars/XexanTerxcin/Bricked-TP-Link-WR840N-V6.20-Recovery-Tool?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/XexanTerxcin/Bricked-TP-Link-WR840N-V6.20-Recovery-Tool?style=for-the-badge)
![GitHub last commit](https://img.shields.io/github/last-commit/XexanTerxcin/Bricked-TP-Link-WR840N-V6.20-Recovery-Tool?style=for-the-badge)

---

### ⭐ Save Your Router — Save Your Money

</div>

---

# 📖 About

Many routers include a hidden **TFTP Recovery Mode** inside their bootloader, allowing a corrupted or soft-bricked firmware to be restored without opening the device or using a USB-to-TTL adapter.

This repository demonstrates the complete recovery process using the **TP-Link TL-WR840N v6.20** as the example router because it is one of the most widely used home routers in many countries.

Although the included firmware files are specifically prepared for the **TL-WR840N v6.20**, the overall recovery process is nearly identical for many TP-Link routers and several other router brands that support TFTP recovery.

Simply replace the firmware with the correct one for your router model and follow the same steps.

> ⚠️ **Always use firmware that exactly matches your router's hardware version.**

---

## ✨ Features

- ✅ Universal TFTP recovery workflow
- ✅ Uses TP-Link TL-WR840N v6.20 as an example
- ✅ No USB-to-TTL adapter required
- ✅ No serial console required
- ✅ No soldering required
- ✅ Beginner-friendly
- ✅ Easily adaptable to other router models

---

## 📦 Requirements

- TP-Link TL-WR840N **v6.20**
- Windows PC/Laptop
- Ethernet Cable

---

# 🚀 Recovery Guide

## ① Clone this repository

```bash
git clone https://github.com/XexanTerxcin/Bricked-TP-Link-WR840N-V6.20-Recovery-Tool.git
```

Install

```
Tftpd64_Installer_v4.70.exe
```

---

## ② Configure Static IP

| Setting | Value |
|---------|-------|
| IP Address | `192.168.0.66` |
| Subnet Mask | `255.255.255.0` |
| Gateway | *(Leave Empty)* |

---

## ③ Launch Tftpd64

- Open **Tftpd64**
- Select the folder

```
TL-WR840N(EU)_V6.20_201124
```

---

## ④ Connect Router

Connect your computer to any **LAN Port** using an Ethernet cable.

---

## ⑤ Enter Recovery Mode

1. Hold the **RESET** button.
2. Power ON the router.
3. Keep holding RESET until Tftpd64 finishes transferring the firmware.
4. Release RESET.
5. Wait for the router to reboot.

---

# 🎉 Done!

Your router should boot normally after flashing.

---

# 🌍 Using This Guide for Other Routers

The **TP-Link TL-WR840N v6.20** is used only as an example because of its popularity, making it easier for most users to follow along.

If you're recovering a different router:

1. Delete the existing .bin file.
2. Download the correct firmware for your router and hardware version.
2. Copy your router's firmware into the folder.
3. Rename the firmware to:

```text
original.bin
```

4. Run this command in the same directory:

```bash
dd if=original.bin of=tp_recovery.bin bs=512 skip=1
```

The generated

```
tp_recovery.bin
```

is the file Tftpd64 should serve.

5. Start the TFTP server and follow the same recovery process.

> **Note:** Some routers require a different TFTP filename, server IP address, or recovery procedure. Check your router's documentation or bootloader requirements before flashing.
---

## ⚠️ Important

> **Never disconnect power while flashing.**

Doing so may permanently brick the router.

---

<details>
<summary><b>📁 Repository Structure</b></summary>

```text
.
├── Firmware/
├── Tftpd64_Installer_v4.70.exe
├── TL-WR840N(EU)_V6.20_201124/
│   └── tp_recovery.bin
└── README.md
```

</details>

---

<div align="center">

## ⭐ Support

If this project saved your router,

**Please consider giving this repository a ⭐ Star.**

It helps other people find this recovery guide.

---

Made with ❤️ by **XeXaN TeRxCiN**

</div>