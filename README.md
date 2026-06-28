Bisa dibuat lebih khas ZannID: lebih santai, tegas, dan fokus ke developer tanpa klaim yang berlebihan.

⚡ ZannID Baileys | Optimized WhatsApp Multi Device Library

<p align="center">
  <img src="https://i.ibb.co/KpyFG40q/image.jpg" alt="ZannID Baileys" width="100%"/>
</p>/*
 © 2026 ZannID. All Rights Reserved.

 Project  : ZannID Baileys
 Type     : Optimized WhatsApp Multi Device Library
 Creator  : ZannID
 Repository : github.com/zann-owner/ZannID-Baileys

 This project is an optimized fork built on top of Baileys.
 Please respect the original project and every contributor.

 If you use this library in your project,
 don't remove the credits.
 Thanks for supporting open-source ❤️
*/

---

🚀 About

ZannID Baileys adalah library WhatsApp Multi Device yang dikembangkan untuk memberikan pengalaman yang lebih nyaman saat membangun bot WhatsApp.

Project ini berfokus pada optimasi, kestabilan, struktur kode yang mudah dipahami, serta kemudahan integrasi ke berbagai jenis bot maupun aplikasi berbasis Node.js.

Cocok digunakan untuk:

- WhatsApp Bot
- AI Assistant
- Customer Service
- Automation System
- Personal Project
- Enterprise Integration

---

✨ Features

- ⚡ Optimized Multi Device Engine
- 🔐 Pairing Code Support
- 📱 QR Login Support
- 💬 Interactive Message Support
- 📦 Newsletter Support
- 🖼️ Album Message
- 🎞️ Rich Media
- 📋 Carousel & Native Buttons
- 🚀 Lightweight Session Handling
- 🛠️ Easy Integration
- 📚 Clean Project Structure
- 🔄 Better Reconnect Flow
- 🔍 Easier Debugging
- ❤️ Developer Friendly

---

📦 Installation

package.json

{
  "dependencies": {
    "@whiskeysockets/baileys": "npm:@zann-owner/baileys"
  }
}

atau

{
  "dependencies": {
    "@adiwajshing/baileys": "npm:@zann-owner/baileys"
  }
}

Lalu jalankan

npm install

---

💻 Import

ESM

import makeWASocket from "@whiskeysockets/baileys"

CommonJS

const {
    default: makeWASocket
} = require("@whiskeysockets/baileys")

---

🚀 Quick Start

const {
    default: makeWASocket,
    useMultiFileAuthState
} = require("@whiskeysockets/baileys")

const pino = require("pino")

async function start() {

    const { state, saveCreds } =
        await useMultiFileAuthState("./session")

    const sock = makeWASocket({
        auth: state,
        logger: pino({ level: "silent" }),
        printQRInTerminal: false,
        browser: ["ZannID", "Chrome", "1.0.0"]
    })

    sock.ev.on("creds.update", saveCreds)

    sock.ev.on("connection.update", ({ connection }) => {

        if (connection === "open") {
            console.log("✅ Connected using ZannID Baileys")
        }

    })

}

start()

---
## ⚡ Tentang ZannID Baileys

Kami memahami betapa menyebalkannya saat bot sering mengalami **crash**, **bad decrypt**, **logged out**, atau berbagai masalah sesi lainnya. Karena itu, **ZannID Baileys** dikembangkan melalui serangkaian riset, eksperimen, dan optimasi agar lebih stabil, ringan, dan nyaman digunakan.

Dirancang untuk para developer yang menginginkan fondasi WhatsApp Multi Device yang modern, cepat, dan mudah dikembangkan tanpa harus terus-menerus berhadapan dengan bug yang mengganggu.

Tinggalkan base lama yang membatasi, dan bangun proyek WhatsApp yang lebih stabil bersama **ZannID Baileys**.

---
❤️ Credits

- Baileys Developers
- Open Source Contributors
- ZannID

---

**Maintained & Crafted with ☕ by ZannID**