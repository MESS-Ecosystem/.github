# MESS — Development & Contribution Workflow

MESS is a realtime multi-platform messaging ecosystem currently developed and maintained primarily by me — Khush Patel (`khushpatel00`).

This project is not built like a traditional startup product.
It is engineered incrementally, feature-by-feature, with the backend architecture always taking first priority.

The goal of MESS is not to ship fast.
The goal is to build a stable realtime messaging architecture that scales properly while still feeling modern, expressive, and platform-native across Web, iOS/iPadOS, and Android.

---

# Core Philosophy

MESS follows a strict backend-first development workflow.

Every feature is designed and stabilized on the server before any client implementation begins.

This prevents:

* client-specific architecture drift
* inconsistent socket contracts
* unstable realtime behavior
* platform desynchronization

The backend is considered the source of truth for the entire ecosystem.

---

# Official Development Flow

## 1. Backend Development (Highest Priority)

All features start on the Node.js + Socket.IO backend.

This includes:

* event architecture
* realtime flows
* room lifecycle
* authentication
* persistence
* scalability decisions
* payload structures
* notification logic
* reconnect behavior

Before any frontend implementation begins, all features must first:

* work correctly on the server
* be manually tested
* pass realtime validation

Testing tools:

* Postman
* Hoppscotch
* Socket.IO testing clients

The server is refined continuously during the entire lifecycle of the feature.

---

## 2. Web Client (Next.js)

After backend validation succeeds, the feature is implemented on the Web client first.

Why?
Because the web client is:

* the fastest iteration environment
* easiest for debugging realtime systems
* easiest for inspecting payloads and socket behavior

The web client acts as the first real-world implementation layer above the backend.

---

## 3. iOS Development

Once stable on Web, the feature is implemented on iOS.

The iOS client is currently the highest-priority frontend platform in the MESS ecosystem.

It is used as:

* the reference-quality client
* the design consistency layer
* the premium UX benchmark

The iOS app is constantly refined even after features are shipped elsewhere.

---

## 4. iPadOS Support

iPadOS support is handled after iPhone implementation.

Currently:

* mostly responsiveness refinements
* layout scaling
* large-screen adjustments
* multitasking compatibility

The architecture remains shared with iOS.

---

## 5. Android Development

Android implementation happens after:

* backend stabilization
* web implementation
* iOS implementation

The Android client is currently heavily AI-assisted / vibe-coded during rapid iteration phases.

Android architecture and UI direction are still supervised carefully, but development speed is prioritized while the backend evolves rapidly.

The Android app follows:

* Material 3 Expressive
* Android 16 expressive motion
* physics-based motion systems
* dynamic color architecture

---

# Refinement Process

After features are implemented across platforms:

## Backend Refinement

The backend is revisited and optimized based on:

* real client behavior
* latency observations
* race conditions
* reconnection edge cases
* socket lifecycle bugs
* persistence issues

The server is never considered “done”.

Realtime systems evolve continuously.

---

## Frontend Refinement

After backend stabilization:

* Web receives refinement
* iOS receives continuous refinement
* Android parity improvements continue afterward

The iOS client currently receives the most UX refinement attention after the backend itself.

---

# Infrastructure

Current infrastructure setup:

## Main Server

Primary hosting currently runs on my own Linux machine for lower latency and faster realtime behavior.

Technologies:

* Arch Linux
* PM2
* Tailscale Funnel
* Socket.IO
* MongoDB Atlas

This acts as the main active backend environment.

---

## Backup Hosting

Render is currently used as:

* fallback deployment
* stability backup
* public redundancy layer

This allows the ecosystem to remain reachable even if the primary self-hosted server is unavailable.

---

# Contribution & Collaboration

MESS is currently a personal long-term engineering project.

External collaboration is welcome, especially for:

* Android development
* frontend refinement
* realtime architecture ideas
* performance improvements
* UI/UX feedback
* testing

However:

Please contact me before making major contributions or architectural decisions.

GitHub profile:
`khushpatel00`

Contact details are available directly on my profile page.

---

# Current Focus Areas

Active engineering priorities currently include:

* DM architecture
* realtime presence systems
* scalable notification routing
* unread state management
* persistence reconciliation
* offline-first behavior
* expressive motion systems
* session architecture
* push notification infrastructure

---

# Final Note

MESS is not trying to become “just another chat app”.

This project exists primarily as:

* a realtime systems engineering project
* a platform architecture experiment
* a multi-client synchronization ecosystem
* a long-term learning and engineering journey

Everything is built incrementally, carefully, and intentionally.

Even the chaos is part of the architecture.
