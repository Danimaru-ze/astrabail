# ✨ AstraBail ✨

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/Danimaru-ze/AstraBail)
[![Author](https://img.shields.io/badge/creator-Danimaru--ze-blueviolet.svg)](https://github.com/Danimaru-ze)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

**AstraBail** is a professional, high-performance WhatsApp Web API library built on top of Baileys, customized and optimized by **Danimaru-ze**. Designed for speed, stability, and ease of use in modern bot ecosystems.

---

## 🚀 Features

- **Turbo Connection**: Optimized handshake and initialization logic for instant bot readiness.
- **Low Latency**: Minimized I/O overhead and efficient memory management.
- **Enhanced MD Support**: Robust handling of Multi-Device sessions and metadata.
- **Custom Branding**: Fully brandable for your own project needs.
- **Automated Sync**: Advanced control over message history and metadata synchronization.

---

## 📦 Installation

To use AstraBail in your project, simply point your dependency to the local folder or host it on your Git:

```json
"dependencies": {
  "astrabail": "file:./AstraBail"
}
```

---

## 🛠️ Usage

```javascript
import { makeWASocket, useMultiFileAuthState } from 'astrabail'

const { state, saveCreds } = await useMultiFileAuthState('./session')

const conn = makeWASocket({
    auth: state,
    printQRInTerminal: true,
    // AstraBail specific optimizations
    fireInitQueries: true,
    syncFullHistory: false
})

conn.ev.on('connection.update', (update) => {
    const { connection } = update
    if(connection === 'open') {
        console.log('AstraBail: Connection Secured! ⚡')
    }
})
```

---

## 💎 Design Philosophy

AstraBail is built with the "Astra" aesthetic in mind—sleek, fast, and powerful. Every part of the library is tuned to provide the most responsive experience for bot developers.

---

## 👨‍💻 Creator

Developed with ❤️ by **Danimaru-ze**.

- **GitHub**: [@Danimaru-ze](https://github.com/Danimaru-ze)
- **WhatsApp**: [Click to Chat](https://wa.me/6289525459709)

---

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.
