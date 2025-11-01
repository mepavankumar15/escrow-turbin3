# Atomic Swap Escrow

A trustless token swap program built on Solana using Anchor 0.32.0. Two parties can exchange tokens with guaranteed settlement through an on-chain escrow mechanism.

---

## 🎯 Overview

This program implements a non-custodial escrow that enables atomic token swaps between two parties:
- **Maker** deposits Token A into a vault, expecting to receive Token B
- **Taker** accepts the offer by sending Token B and receiving Token A
- Either party can **refund** if the swap doesn't complete

No intermediary needed. Everything is validated and executed on-chain.

---

## 📊 Transaction Details

### Token Mints Created
| Token | Address |
|-------|---------|
| **Maker Token (A)** | `BtvqHCDCCu9mm8pS1vRTrkw9CMeBu5yxbjmPTuc7ArK` |
| **Taker Token (B)** | `EJSbIEjbwxg3q9NhEAkfMvVKTY6YhvtwkESRLqEyAhp7` |

### Vault Account (Tokens Locked)
- **Vault PDA**: Escrow-controlled token account
- **Tokens Locked**: 1,000 (Maker Token)
- **Status**: 🔐 Secure (only escrow can authorize transfers)

### Escrow Completion
- **Instruction**: `make`
- **Transaction Hash**: `2PvAEavJzLjeL VPqum92Mx2RiwyAXm8SzKmf6dgf9jcmexsqp8yzFUTAcSfwdXwPGmdS96VMQTgrV3tBSUAUsHKG`
- **Status**: ✅ Confirmed on-chain

---

## 📸 Test Execution Screenshot

![Escrow Transaction Hash](./escrow-txhash.jpg)

**Screenshot shows:**
- ✅ Maker Mint: `BtvqHCDCCu9mm8pS1vRTrkw9CMeBu5yxbjmPTuc7ArK`
- ✅ Taker Mint: `EJSbIEjbwxg3q9NhEAkfMvVKTY6YhvtwkESRLqEyAhp7`
- ✅ Make TX: `2PvAEavJzLjeL VPqum92Mx2RiwyAXm8SzKmf6dgf9jcmexsqp8yzFUTAcSfwdXwPGmdS96VMQTgrV3tBSUAUsHKG`
- ✅ Escrow successfully created and tokens locked

---

## 🚀 Quick Start

### Prerequisites
- Rust 1.70+
- Anchor 0.32.0
- Solana CLI
- Node.js 16+

### Installation

