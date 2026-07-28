# 🔧 TP-Link TL-WR840N v6.20 Recovery (TFTP Method)

Recover your **TP-Link TL-WR840N v6.20** from a soft brick using the built-in **TFTP Recovery Mode**—**no USB-to-TTL adapter required**.

> **Tested on:** TL-WR840N v6.20

---

## 📋 Requirements

- TP-Link TL-WR840N v6.20
- Ethernet cable
- PC/Laptop
- Tftpd64/Tftpd32
- Official TP-Link firmware

---

## 🚀 Recovery Steps

### 1️⃣ Clone this repository

```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

### 2️⃣ Install Tftpd64 (Windows)

Download and install **Tftpd64** (or **Tftpd32**).

### 3️⃣ Set a Static IP

Configure your Ethernet adapter:

| Setting | Value |
|---------|-------|
| IP Address | `192.168.0.66` |
| Subnet Mask | `255.255.255.0` |
| Gateway | Leave blank |

### 4️⃣ Open Tftpd64

- Launch **Tftpd64**
- Select the directory containing the recovery firmware.
- Make sure the firmware filename matches the one expected by the bootloader.

### 5️⃣ Connect the Router

Connect your PC to any **LAN** port of the router using an Ethernet cable.

### 6️⃣ Start Recovery Mode

1. Press and **hold the Reset button**.
2. While holding it, **power on the router**.
3. Keep holding the button until Tftpd64 shows the firmware transfer has completed successfully.
4. Release the button.

### 7️⃣ Wait

The router will automatically flash the firmware and reboot.

✅ Recovery Complete!

---

## ⚠️ Notes

- Use the correct firmware for your hardware version.
- Do **not** disconnect power during flashing.
- The first boot may take a few minutes.

---

## ❤️ Credits

Thanks to the TP-Link community and everyone who shared recovery methods that helped bring this router back to life.

---

⭐ If this guide helped you recover your router, consider giving this repository a **Star**.
