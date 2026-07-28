<div align="center">

# 🔧 TP-Link TL-WR840N v6.20 Recovery Tool

### Recover your **TP-Link TL-WR840N v6.20** using the built-in **TFTP Recovery Mode**
### 🚫 No USB to TTL Adapter Required

![GitHub Repo stars](https://img.shields.io/github/stars/XexanTerxcin/Bricked-TP-Link-WR840N-V6.20-Recovery-Tool?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/XexanTerxcin/Bricked-TP-Link-WR840N-V6.20-Recovery-Tool?style=for-the-badge)
![GitHub last commit](https://img.shields.io/github/last-commit/XexanTerxcin/Bricked-TP-Link-WR840N-V6.20-Recovery-Tool?style=for-the-badge)

---

### ⭐ If this repository helps you, don't forget to Star it!

</div>

---

## ✨ Features

- ✅ Recover a soft-bricked TL-WR840N v6.20
- ✅ Uses the built-in TP-Link TFTP Recovery
- ✅ No serial console required
- ✅ No soldering required
- ✅ Beginner-friendly

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

# ⚠️ Using Another Router?

If your router is **NOT TL-WR840N v6.20**

1. Delete the existing `.bin` file.
2. Copy your own firmware into the folder.
3. Rename it to

```
original.bin
```

Run this command in the same directory

```bash
dd if=original.bin of=tp_recovery.bin bs=512 skip=1
```

The generated

```
tp_recovery.bin
```

is the file Tftpd64 should serve.

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

## ❤️ Credits

- TP-Link
- OpenWrt Community
- Everyone who documented TP-Link recovery methods

---

<div align="center">

## ⭐ Support

If this project saved your router,

**Please consider giving this repository a ⭐ Star.**

It helps other people find this recovery guide.

---

Made with ❤️ by **XeXaN TeRxCiN**

</div>