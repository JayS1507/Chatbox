# Aegis Chat 🔐  
### *Beyond Encryption: Security Against Coercion*  

<div align="center">  
<img src="https://raw.githubusercontent.com/user-attachments/assets/9b106a72-68f1-4f11-85fd-91a9b1c77f8d" alt="Aegis Chat Logo" width="150">  
</div>  

<div align="center">  

[![License](https://img.shields.io/github/license/your-username/aegis-chat?color=blue)](LICENSE)  
[![Hackathon](https://img.shields.io/badge/Hackathon-International%20Hackathon%20Name-orange)](#)  
[![Tech](https://img.shields.io/badge/Frontend-VanillaJS%20%7C%20TailwindCSS-green)](#)  
[![Crypto](https://img.shields.io/badge/Crypto-JSEncrypt.js-lightgrey)](#)  
[![Contributions](https://img.shields.io/badge/PRs-Welcome-brightgreen.svg)](CONTRIBUTING.md)  

</div>  

---

## 💡 What happens when encryption isn't enough?  

We trust our most private conversations to "secure" apps. End-to-end encryption is powerful, but it has a **fatal flaw**:  

👉 An attacker doesn’t need to break the world’s strongest encryption.  
👉 They just need to **break you**.  

If someone forces you to unlock your phone, your "secure" messenger collapses instantly.  

That’s not a **security flaw**; it’s a **reality flaw**.  
And we decided to fix it.  

---

## ✨ Introducing *Decoy Mode*: Plausible Deniability  

**Aegis Chat** is a proof-of-concept messenger that defends against **coercion attacks** using a dual-password system:  

🔑 **Real Password** → Unlocks your *real, sensitive* conversations.  
🤫 **Decoy Password** → Unlocks a *benign, fake* set of conversations.  

An adversary sees a **fully functional messenger**.  
They’ll never know your real chats exist.  

You don’t just get encryption.  
You get an **escape route**.  

---

## 🚀 Live Demo (No Install Required)  

1. Clone this repository and open the file:  

```bash
git clone https://github.com/your-username/aegis-chat.git
cd aegis-chat
open aegis-chat-decoy.html   # Or double-click to open in browser
```  

2. Open the file in **two separate browser tabs**.  

3. **Create Identities:**  
   - In Tab 1 → Register user `alice` with a REAL + DECOY password.  
   - In Tab 2 → Register user `bob` with a REAL + DECOY password.  

4. **Secret Chat:**  
   - Log in using **real passwords** in both tabs.  
   - Enjoy an *end-to-end encrypted* private conversation.  

5. **Decoy Chat:**  
   - Log out and log back in using **decoy passwords**.  
   - The secret chat is gone—replaced by a separate, harmless chat space.  

🎭 You’ve just witnessed **plausible deniability** in action.  

---

## 🛠️ Under the Hood  

This isn’t a UI trick—the security is **built into the cryptographic core**.  

### 🔐 Dual-Reality Authentication  
- The password you use defines which **cryptographic context** is loaded.  
- From the very first step, two realities remain completely isolated.  

### 📂 Cryptographically Separated Data  
- Each message is **end-to-end encrypted** and tagged with its context (`primary` or `decoy`).  
- The loaded private key can **only decrypt** its own context.  

Example stored message:  

```json
{
  "id": "1678886400000",
  "sender": "alice",
  "receiver": "bob",
  "context": "primary", // or "decoy"
  "content": "U2FsdGVkX1... (Encrypted for Receiver)",
  "contentForSender": "U2FsdGVkX1... (Encrypted for Sender)"
}
```  

---

## 💻 Technology Stack  

- **Frontend** → Vanilla JavaScript (ES6), HTML5, Tailwind CSS  
- **Cryptography** → [JSEncrypt.js](https://github.com/travist/jsencrypt) (RSA 1024-bit, optimized for PoC)  
- **Backend Simulation** → Browser Local Storage (to demo client-side cryptography without a server)  

---

## 🗺️ Roadmap  

🔹 **Phase 1: Production-Ready Backend**  
- Secure Node.js + WebSocket backend  
- Password hashing with **Argon2**  

🔹 **Phase 2: Mobile Application**  
- Progressive Web App (PWA)  
- Native iOS & Android clients  

🔹 **Phase 3: Security Audit**  
- Third-party audit of cryptographic design & implementation  
- Public release after validation  

---

## 🎯 Why This Matters  

Most secure messengers **ignore coercion scenarios**.  
Aegis Chat introduces **plausible deniability as a core feature**.  

✔️ Protects against *physical threats*  
✔️ Provides a *believable decoy environment*  
✔️ Extends security **beyond encryption**  

---

## 📸 Screenshots  

*(Add here once you capture UI images of real vs decoy mode!)*  

---

## 🤝 Contributing  

We welcome contributions!  

1. Fork this repo  
2. Create your feature branch:  
   ```bash
   git checkout -b feature/amazing-feature
   ```  
3. Commit changes:  
   ```bash
   git commit -m "Add amazing feature"
   ```  
4. Push to branch:  
   ```bash
   git push origin feature/amazing-feature
   ```  
5. Open a Pull Request 🚀  

---

## 📜 License  

This project is released under the **MIT License**.  
Free to use, modify, and distribute.  

---

## 🏆 Hackathon Project  

Developed for **[International Hackathon Name]** 🥇  
Showcasing *next-generation secure messaging with coercion resistance*.  
