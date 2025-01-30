# Cozy

Cozy is an innovative mobile application designed to provide users with personalized, context-aware AI agents. Each user is paired with a unique agent, equipped with its own Bitcoin wallet, enabling seamless agent-to-agent transactions. Additionally, agents can interact with the NOSTR protocol to search for items or data shared by users on NOSTR clients, enhancing the overall user experience.

## Features

- **Personalized Agents**: Each user is assigned a unique agent that can be customized with names, avatars, and traits, providing a personalized experience.
- **Integrated Bitcoin Wallets**: Every agent comes with its own Bitcoin wallet, allowing for secure and straightforward transactions.
- **Agent-to-Agent Transactions**: Facilitates direct transactions between agents, streamlining the process for users.
- **NOSTR Protocol Integration**: Agents can search for items or data shared by users on NOSTR clients, expanding the scope of information accessible within the app.

## Technical Overview

Cozy is developed using **React Native** with **Expo**, ensuring a smooth and responsive user experience across various devices. The integration of **Three.js** allows for interactive and engaging agent representations. The app employs secure methods for Bitcoin wallet management and transactions, adhering to industry best practices.


For your MVP, you'll need a **stack that supports Web3/Nostr authentication, 3D rendering, Bitcoin Lightning transactions, and a game-like UI**. Here's the best tech stack for your needs:

---

### **Tech Stack for Your 3D Nostr-Powered Web App**

#### **Frontend**
- **Framework:** **React.js** (component-based and works well with your needs)
- **3D Rendering:** **React Three Fiber** (Three.js for React, ideal for managing your 3D scene)
- **State Management:** **Zustand** (lightweight and great for UI/game-like state)
- **Styling/UI:** **Tailwind CSS + Radix UI** (easy-to-use styling with a modern feel)
- **Game UI Elements:** **Phosphor Icons / Lucide Icons** (for game-like UI elements)

#### **Backend**
- **Nostr Integration:**  
  - **Nostr Tools:** **nostr-js or nostr-sdk** (to handle authentication and messaging)  
  - **Relays:** Use **public Nostr relays** for searching items and verifying transactions.
  
- **Bitcoin Lightning Transactions:**  
  - **LNBits API or LND/CLN with a WebSocket connection** (to display Bitcoin balance and process transactions)  
  - **Breez SDK** (for a simple user-side wallet integration)

- **Agent Journal (Storage)**
  - **IndexedDB or Firebase Firestore** (to store transaction receipts locally or in the cloud)

#### **Game-Style UI Components**
- **Agent Avatar & Stats UI:**  
  - **React Three Fiber HUD** for overlaying health, sats balance, and journal UI  
  - **Framer Motion** (for smooth animations)

#### **Deployment**
- **Hosting:** **Vercel or Netlify** (fast, free-tier-friendly for MVP)
- **Database (Optional, if you need persistence):** **Supabase** (PostgreSQL with WebSockets, great for real-time updates)

---

### **Key Features and Implementation Plan**
1. **Nostr Login** → Use **nostr-js** for signing users in.
2. **Customize AI Agent (Pawn)** → Store user preferences in Zustand/local storage.
3. **Bitcoin Wallet Balance** → Fetch from LNBits or a Lightning provider.
4. **AI Agent Nostr Search** → Query relays for items listed for sale.
5. **Confirm Lightning Payment** → Process via LNBits/Breez SDK and store receipt.
6. **Game-Style UI (Home Screen)** → Display agent, health, balance, and journal.
7. **Agent Journal (Transaction History)** → Display transactions with timestamps.

---
