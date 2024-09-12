## Solana Active Wallet React

This is a react hook that detects a user's current active solana wallet on the client. It detects when a user has changed their active wallet inside a browser wallet extension.
The wallets currently supported are:
- Phantom
- Backpack

Support for other wallets will be added in the future.

### Note the hook relies on the "publicKey" returned by the useWallet hook from @solana/wallet-adapter-react to get its initial value

### Demo

[Demo](https://solana-active-wallet-react-demo.vercel.app/)

### Installation

```bash
npm install solana-active-wallet-react
```

### Usage

```tsx
import useSolanaActiveWallet from "solana-active-wallet-react";
import { useWallet } from "@solana/wallet-adapter-react";

const { publicKey } = useWallet();
const { activePublicKey, phantomProvider, backpackProvider } = useSolanaActiveWallet(publicKey);
```