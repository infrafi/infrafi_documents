---
icon: checklist
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Prerequisites

Before you start using InfraFi Protocol, make sure you have everything set up correctly. This guide will walk you through all requirements.

{% hint style="warning" %}
**Testnet Environment**: These instructions are for OORT testnet only. Never use real mainnet assets with testnet contracts.
{% endhint %}

## Required Setup

### 1. 🌐 **Web3 Wallet Configuration**

You need a Web3 wallet connected to the OORT testnet:

#### **Recommended Wallets**
- **MetaMask** (Most popular, best support)
- **WalletConnect** compatible wallets
- **Coinbase Wallet**
- **Trust Wallet**

#### **Add OORT Testnet to Your Wallet**
```
Network Name: OORT Testnet
RPC URL: https://mainnet-rpc.oortech.com
Chain ID: 970
Currency Symbol: OORT
Block Explorer: https://mainnet-scan.oortech.com
```

#### **Manual Setup Instructions**
1. Open your wallet and go to network settings
2. Click "Add Network" or "Custom RPC"
3. Enter the details above
4. Save and switch to OORT Testnet

### 2. 🏗️ **OORT Node Ownership**

You must own and control at least one OORT node:

#### **Node Requirements**
- ✅ **Active Registration** - Node must be registered in OORT network
- ✅ **Ownership Verified** - Your wallet must be the registered owner
- ✅ **Operational Status** - Node should be active and earning rewards
- ✅ **Minimum Age** - Node should have operational history (recommended)

#### **Verify Node Ownership**
1. Visit [OORT Network Explorer](https://mainnet-scan.oortech.com)
2. Search for your node ID
3. Confirm your wallet address is listed as owner
4. Check node status and earning history

### 3. 💰 **Testnet Tokens**

You need OORT testnet tokens for gas fees:

#### **Get Testnet OORT**
- **OORT Faucet**: [https://faucet.oortech.com](https://faucet.oortech.com)
- **Amount Needed**: 0.1 OORT minimum (recommended: 0.5 OORT)
- **Usage**: Transaction fees for deposits, borrows, repayments

#### **WOORT Testnet Tokens**
You'll also need WOORT tokens for testing borrowing:
- Available through OORT testnet faucets
- Used as the borrowing currency
- No real value - testnet tokens only

### 4. 📱 **Browser & Device**

#### **Supported Browsers**
- ✅ **Chrome** (Recommended)
- ✅ **Firefox** 
- ✅ **Safari** (with some limitations)
- ✅ **Brave**

#### **Device Requirements**
- Desktop or laptop recommended for first use
- Mobile browsers supported but may have wallet connection issues
- Stable internet connection required
- JavaScript enabled

## Knowledge Prerequisites

### 🎓 **Recommended Understanding**

#### **DeFi Basics**
- How lending protocols work
- Understanding of collateral and loans
- Concepts of liquidation and loan-to-value ratios
- Basic Web3 wallet usage

#### **DePIN Concepts**
- What are Decentralized Physical Infrastructure Networks
- How node ownership and rewards work
- Understanding of infrastructure tokenomics

#### **Risk Awareness**
- Smart contract risks and limitations
- Liquidation mechanisms and prevention
- Interest rate calculations
- Network and protocol dependencies

### 📚 **Learning Resources**
If you're new to these concepts:
- **[What is InfraFi?](../overview/)** - Start here for basics
- **[Key Features](../overview/key-features.md)** - Understand core functionality
- **[Glossary](../resources/glossary.md)** - Learn terminology
- **DeFi Education** - External resources on decentralized finance

## Security Setup

### 🔒 **Wallet Security**

#### **Best Practices**
- ✅ **Secure Seed Phrase** - Store recovery phrase safely offline
- ✅ **Strong Password** - Use unique, complex wallet password  
- ✅ **Hardware Wallet** - Consider hardware wallet for larger amounts
- ✅ **Regular Backups** - Keep multiple secure copies of recovery info

#### **Transaction Safety**
- Always verify contract addresses before transactions
- Double-check transaction details before confirming
- Start with small amounts to test functionality
- Monitor gas fees and network congestion

### 🛡️ **Node Security**

#### **Protect Your Nodes**
- ✅ **Secure Private Keys** - Keep node management keys safe
- ✅ **Regular Monitoring** - Check node status and performance
- ✅ **Backup Critical Data** - Maintain copies of important node information
- ✅ **Network Security** - Ensure node infrastructure is properly secured

## Pre-Flight Checklist

Before proceeding to the [Quick Start Guide](quickstart.md), verify:

### ✅ **Wallet Setup**
- [ ] Web3 wallet installed and configured
- [ ] OORT testnet network added and selected
- [ ] Testnet OORT tokens acquired for gas fees
- [ ] Wallet connection tested on OORT network

### ✅ **Node Verification**  
- [ ] OORT node ownership confirmed on blockchain
- [ ] Node operational status verified
- [ ] Node ID and details recorded for reference
- [ ] Understanding of node value and earning history

### ✅ **Knowledge Check**
- [ ] Basic DeFi lending concepts understood
- [ ] InfraFi proxy custody mechanism comprehended
- [ ] Liquidation risks and prevention strategies known
- [ ] Safety guidelines and best practices reviewed

### ✅ **Security Preparation**
- [ ] Wallet security measures implemented  
- [ ] Transaction verification process established
- [ ] Emergency procedures understood
- [ ] Support resources bookmarked

## Common Setup Issues

### 🔧 **Troubleshooting**

#### **Network Connection Problems**
```
Error: "Network not found" or "RPC Error"
Solution: Verify RPC URL and chain ID are exactly as specified
```

#### **Wallet Connection Issues**
```
Error: "Wallet not connecting" or "Provider error"  
Solution: Refresh page, disconnect/reconnect wallet, check network selection
```

#### **Node Ownership Verification**
```
Error: "Node not owned by user"
Solution: Double-check node ID, verify ownership on OORT explorer
```

#### **Insufficient Gas Fees**
```
Error: "Transaction failed" or "Out of gas"
Solution: Acquire more testnet OORT tokens from faucet
```

## Getting Help

If you encounter issues during setup:

### 💬 **Community Support**
- **Discord**: Real-time help in #support channel
- **GitHub Issues**: Technical problems and bug reports
- **Community Forum**: Setup questions and discussions

### 📖 **Documentation**
- **[FAQ](../resources/faq.md)**: Common questions and solutions
- **[Troubleshooting Guide](../guides/position-management.md#troubleshooting)**: Detailed problem-solving
- **[Community Links](../resources/community.md)**: Additional support resources

---

## Ready to Continue?

Once you've completed all prerequisites:

🚀 **[Start the Quick Start Guide](quickstart.md)** - Make your first transaction

or

📚 **[Learn More About Safety](safety-guidelines.md)** - Best practices and risk management

---

*Having trouble with setup? Don't hesitate to ask for help in our community channels!*
