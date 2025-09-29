---
icon: bolt
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

# QuickStart Guide

Get started with InfraFi in 5 minutes! Learn how to use your DePIN nodes as collateral to borrow tokens.

## What is InfraFi?

InfraFi is a decentralized lending protocol that lets you **use your physical infrastructure devices (DePIN nodes) as collateral** to borrow tokens. Think Compound Finance, but for hardware assets like OORT nodes, Helium miners, and Filecoin storage devices.

### Core Concept
```
Your OORT Node → Deposit as Collateral → Borrow WOORT Tokens → Earn Yield
```

{% hint style="success" %}
**Key Benefit**: Keep earning from your nodes while accessing liquidity from their value!
{% endhint %}

## Prerequisites

Before you start, make sure you have:

### 🔧 **Required Setup**
- [ ] **OORT Wallet** connected to OORT testnet
- [ ] **OORT Node(s)** that you own and control
- [ ] **WOORT Tokens** (for gas fees and testing)
- [ ] **Web3 Wallet** (MetaMask, WalletConnect compatible)

### 🌐 **Network Configuration**
Add OORT Testnet to your wallet:
```
Network Name: OORT Testnet
RPC URL: https://mainnet-rpc.oortech.com
Chain ID: 970
Currency: OORT
Explorer: https://mainnet-scan.oortech.com
```

{% hint style="info" %}
**First time?** Get OORT testnet tokens from the [OORT Faucet](https://faucet.oortech.com) for testing.
{% endhint %}

## Step-by-Step Process

### Step 1: Connect Your Wallet

1. Navigate to the InfraFi app
2. Click "Connect Wallet"
3. Select your wallet provider
4. Switch to OORT Testnet when prompted

### Step 2: Deposit Your OORT Node

{% hint style="warning" %}
**Testnet Only**: This guide uses testnet contracts. Never deposit mainnet assets to testnet contracts!
{% endhint %}

1. **Go to "Deposit" page**
2. **Enter your node details**:
   - Node ID: Your OORT node identifier
   - Node Type: `1` (for OORT protocol)
3. **Approve the transaction**:
   - Your node ownership will be transferred to InfraFi's secure proxy
   - You maintain all earning rights
   - Node continues operating normally

```javascript
// Example: Node deposit transaction
Contract: 0x74f68Eec49DFAd34E22f3f6F3e38d4d92D8ab676
Function: depositNodes([nodeId], [nodeType])
Parameters: 
  - nodeIds: [123456789]  // Your node ID
  - nodeTypes: [1]        // OORT protocol type
```

### Step 3: Borrow Against Your Collateral

1. **Check your collateral value**:
   - View your deposited node's current value
   - See available borrowing capacity (up to 80% LTV on testnet)

2. **Borrow WOORT tokens**:
   - Enter amount to borrow (within your limit)
   - Review interest rate (starts at 3% APY)
   - Confirm transaction

```javascript
// Example: Borrow transaction
Contract: 0x74f68Eec49DFAd34E22f3f6F3e38d4d92D8ab676
Function: borrow(amount)
Parameters:
  - amount: 1000000000000000000  // 1 WOORT (18 decimals)
```

### Step 4: Manage Your Position

**Monitor your loan**:
- Current debt amount
- Interest accrued
- Loan-to-value ratio
- Liquidation risk level

**Repay when ready**:
- Partial or full repayment anytime
- Interest calculated per block
- Approve WOORT spending first

### Step 5: Withdraw Your Node

Once your loan is fully repaid:
1. **Verify zero debt balance**
2. **Click "Withdraw Node"**
3. **Confirm transaction**
4. **Node ownership returns to you**

## Example Transaction Flow

Here's what a complete cycle looks like:

```bash
# 1. Initial State
Your OORT Node: Worth 1000 WOORT
Your WOORT Balance: 0

# 2. After Deposit
Node Status: Deposited to InfraFi
Available to Borrow: 800 WOORT (80% LTV)

# 3. After Borrowing 500 WOORT
Your WOORT Balance: 500 WOORT
Your Debt: 500 WOORT + interest
LTV: 50% (healthy)

# 4. After Repaying 520 WOORT (principal + interest)
Your WOORT Balance: -20 WOORT (paid interest)
Your Debt: 0 WOORT
Node Status: Ready to withdraw
```

## Contract Addresses (OORT Testnet)

{% hint style="danger" %}
**Testnet Only**: These are testnet contracts for testing purposes only!
{% endhint %}

```
Main Vault: 0x74f68Eec49DFAd34E22f3f6F3e38d4d92D8ab676
WOORT Token: 0x0809f1dC272F42F96F0B06cE5fFCEC97cB9FA82d
OORT Nodes: 0xA97E5185DC116588A85197f446Aa87cE558d254C

Network: OORT Testnet (Chain ID: 970)
Explorer: https://mainnet-scan.oortech.com
```

## Safety & Best Practices

### 🛡️ **Risk Management**
- **Monitor LTV**: Keep below 70% to avoid liquidation risk
- **Track Interest**: Interest accrues every block
- **Reserve Funds**: Keep WOORT for repayment + gas fees
- **Node Health**: Ensure your nodes keep operating normally

### ⚠️ **Important Warnings**
- **Testnet Only**: Never use real assets on testnet
- **Liquidation Risk**: Loans can be liquidated if LTV > 80%
- **Smart Contract Risk**: Protocol is experimental
- **Node Ownership**: InfraFi controls node during deposit

## Troubleshooting

### Common Issues:

**"Node not owned by user"**
- Verify you own the node in OORT's system
- Check node ID is correct
- Ensure node isn't already deposited elsewhere

**"Insufficient collateral"**
- Check your node's current value
- Verify LTV limits (80% max on testnet)
- Try borrowing a smaller amount

**"Transaction failed"**
- Ensure sufficient OORT for gas
- Check network connection to OORT testnet
- Try increasing gas limit

## What's Next?

### 📚 **Learn More**
- [Technical Architecture](broken-reference) - How InfraFi works under the hood
- [Risk Assessment](broken-reference) - Understanding liquidation and risks
- [Advanced Features](broken-reference) - Position management and optimization

### 🛠️ **For Developers**
- [Integration Guide](broken-reference) - Build on InfraFi
- [API Documentation](broken-reference) - Contract interfaces
- [GitHub Repository](https://github.com/infrafi/infrafi_contracts) - Source code

### 🤝 **Join the Community**
- [Discord](https://discord.gg/infrafi) - Get support and discuss
- [Governance](broken-reference) - Participate in protocol decisions
- [Bug Reports](https://github.com/infrafi/infrafi_contracts/issues) - Report issues

{% hint style="success" %}
**Congratulations!** You've successfully used InfraFi to unlock liquidity from your DePIN assets. Welcome to the future of infrastructure finance! 🚀
{% endhint %}
