Here's a revised version of the README.md with improved clarity, formatting, and readability: 

---

# Mostro Web

A super-early version of a web client for the [Mostro](https://github.com/MostroP2P/mostro) P2P system.

This project provides a web interface for peer-to-peer Bitcoin trading over the Lightning Network ⚡️, leveraging **nostr** 🦩. The Lightning Network is a layer 2 solution for Bitcoin that enables fast and low-cost transactions.

---

## Prerequisites

### Node.js and NPM
- **Node.js**: Recommended version: `v20.15.1`
- **NPM**: Recommended version: `10.7.0`

### Mostro
- Clone the [Mostro](https://github.com/MostroP2P/mostro) repository.
- Follow the detailed setup instructions [here](https://github.com/MostroP2P/mostro?tab=readme-ov-file#requirements).

---

## Installation

### 1. Clone the Repository
```bash
git clone git@github.com:MostroP2P/mostro-web.git
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure Environment Variables
1. Create a new `.env` file by copying the sample file:
   ```bash
   cp .env-sample .env
   ```
2. Set the following environment variables:
   - **RELAYS**: A comma-separated list of relay URLs. Example:
     ```bash
     RELAYS=wss://relay.mostro.network,wss://relay.nostr.net
     ```
   - **MOSTRO_PUB_KEY**: The public key of the Mostro daemon to interact with. This should match the private key (nsec) used in Mostro. Example:
     ```bash
     MOSTRO_PUB_KEY=npub19m9laul6k463czdacwx5ta4ap43nlf3lr0p99mqugnz8mdz7wtvskkm5wg
     ```
    Read how to get a Mostro Pub Pey at the [Mostro daemon repository](https://github.com/MostroP2P/mostro).

3. Load the environment variables:
   ```bash
   source .env
   ```

> **Note**: It’s also possible (and sometimes preferable) to run a private relay. Instructions for doing this using Docker are available in the [Mostro documentation](https://github.com/MostroP2P/mostro?tab=readme-ov-file#option-1-run-mostro-with-a-private-dockerized-relay).

### 4. Start the Development Server
```bash
npm run dev
```

---

## Features

- ✅ Post buy and sell orders.
- ✅ View order lists.
- ✅ Decode direct messages (DMs) from Mostro.
- ✅ Buy flow:
  - Maker/market rate
  - Maker/fixed price
  - Taker/market rate
  - Taker/fixed price
- ✅ Sell flow:
  - Maker/market rate
  - Maker/fixed price
  - Taker/market rate
  - Taker/fixed price
- ✅ Handle multiple relays.
- ✅ Key management using NIP-07.
- ✅ Persist old events.
- ✅ Direct messaging with peers.
- ✅ Dispute management.
- 🔲 **NIP-59 support** (Coming soon!)

---

## Nuxt.js Scripts

This is a **Nuxt 3** project, which includes the following scripts for development, production builds, and static site generation:

- **Run in development mode** (hot reload):
  ```bash
  npm run dev
  ```
- **Build for production**:
  ```bash
  npm run build
  ```
- **Start the production server**:
  ```bash
  npm run start
  ```
- **Generate a static release**:
  ```bash
  npm run generate
  ```

> **Tip**: Run `npm run build` at least once before starting development with `npm run dev`.

---

## License

This project is licensed under the MIT License 📜. For more information, see the [LICENSE](./LICENSE) file.