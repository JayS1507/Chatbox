<div align="center">

<img src="https://raw.githubusercontent.com/user-attachments/assets/9b106a72-68f1-4f11-85fd-91a9b1c77f8d" alt="AegisParadox Logo" width="150">

# 🛡️ AegisParadox
### The Shield of Two Realities — Beyond Encryption, Security Against Coercion

</div>

---

## ❓ What happens when encryption isn't enough?
We trust our most private conversations to “secure” apps. End-to-end encryption is hailed as the ultimate shield.  
But there’s a fatal flaw.  

An attacker doesn’t need to break encryption — they just need to break *you*.  
If someone can coerce you into unlocking your phone, your fortress collapses.  

That’s not a *security flaw* — it’s a *reality flaw*.  
And **AegisParadox** fixes it.  

---

## ✨ Introducing: Decoy Mode with Plausible Deniability
**AegisParadox** is a proof-of-concept messenger that protects you *even under coercion*.  

🔑 **Two Passwords. Two Cryptographically Separate Realities.**  

- **Your Real Password** → Unlocks your sensitive conversations.  
- **Your Duress (Decoy) Password** → Unlocks a safe, benign-looking chat space.  

An adversary sees a perfectly functional messenger — with no clue your real chats exist.  

You don’t just get encryption.  
You get an *escape route*.  

---

## 🚀 Live Demo
This is not just theory. You can run it **right now**, no installation required.  

1. Open **`aegisparadox.html`** in two browser tabs.  
2. In Tab 1, register `alice` with a **REAL** password + a **DECOY** password.  
3. In Tab 2, register `bob` the same way.  
4. Log in with **REAL passwords** → start a secret end-to-end encrypted conversation.  
5. Log out, log in with **DECOY passwords** → the secret chat vanishes, replaced by a harmless chat space.  

You've just seen **plausible deniability in action**.  

---

## 🛠️ How It Works (Under the Hood)

### 1. Dual-Reality Authentication
Your login password determines which cryptographic "context" is loaded.  

### 2. Cryptographically Separated Data
Each message is encrypted *and* tagged with its context:  

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

Only the correct key can decrypt the right context. The other one is cryptographically invisible.  

---

## 💻 Technology Stack
- **Frontend:** Vanilla JavaScript (ES6), HTML5, Tailwind CSS  
- **Cryptography:** JSEncrypt.js (RSA 1024-bit, optimized for speed in PoC)  
- **Backend Simulation:** Browser Local Storage → No server required  

---

## 🗺️ Roadmap
**Phase 1:** Production Backend → Node.js + WebSockets + Argon2 password hashing  
**Phase 2:** Mobile App → Progressive Web App (PWA) + native clients  
**Phase 3:** Security Audit → Independent professional cryptographic review  

---

## 🏆 Vision
**AegisParadox** is more than encrypted chat.  
It’s **security against coercion** — a shield that works in both digital and physical worlds.  

Built for the [International Hackathon Name] 🥇  

---

## 📜 License
This project is released under the **MIT License** — free to use, modify, and share.  
