---
icon: book-atlas
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

# Glossary

Essential terminology for understanding InfraFi Protocol and the DePIN + DeFi ecosystem.

## InfraFi-Specific Terms

### **InfraFi Protocol**
The first decentralized lending protocol designed specifically for Decentralized Physical Infrastructure Networks (DePIN), allowing physical device owners to borrow against their infrastructure assets.

### **Proxy-Based Custody**
InfraFi's innovative custody mechanism where smart contract proxies manage on-chain ownership rights while users maintain full operational control of their physical devices.

### **Node Proxy**
Individual smart contracts that hold ownership of DePIN devices on behalf of the vault, enabling custody while preserving operational continuity.

### **Protocol Adapter**
Modular smart contracts that provide integration interfaces for specific DePIN networks (e.g., OORT, Helium, Filecoin), enabling multi-protocol support.

### **Dynamic Asset Valuation**
Real-time pricing system that values DePIN devices based on hardware specifications, staked assets, earned rewards, and network performance metrics.

## DePIN Terminology

### **DePIN (Decentralized Physical Infrastructure Networks)**
Blockchain networks that incentivize individuals to deploy and operate real-world physical infrastructure (wireless, storage, compute, sensors) in exchange for token rewards.

### **Infrastructure Device / Node**
Physical hardware deployed by individuals to participate in DePIN networks, such as wireless hotspots, storage miners, compute servers, or IoT sensors.

### **Node Operator**
Individual or entity that owns, deploys, and operates physical infrastructure devices within DePIN networks to earn token rewards.

### **Network Rewards**
Token incentives earned by node operators for providing infrastructure services like connectivity, storage, or compute resources to the network.

### **Staking**
Process of locking tokens in a DePIN protocol to operate a node or enhance earning potential, often required for network participation.

### **Device Earnings / Node Rewards**
Tokens earned by infrastructure devices for providing network services, typically distributed based on uptime, performance, and demand.

## DeFi Lending Terms

### **Collateral**
Assets deposited to secure a loan. In InfraFi, these are DePIN devices and their associated staked tokens and rewards.

### **Loan-to-Value Ratio (LTV)**
Percentage of collateral value that can be borrowed. Formula: `(Debt ÷ Collateral Value) × 100`

### **Liquidation**
Automatic sale of collateral when a loan becomes unsafe (LTV exceeds threshold), used to repay debt and protect lenders.

### **Liquidation Threshold**
Maximum LTV ratio before liquidation is triggered. InfraFi uses 80% on testnet, planned 60% on mainnet.

### **Interest Rate**
Cost of borrowing, expressed as Annual Percentage Yield (APY). InfraFi uses a dynamic Jump Rate Model.

### **Utilization Rate**
Percentage of available funds currently borrowed. Formula: `Borrows ÷ (Cash + Borrows)`

### **Jump Rate Model**
Interest rate system that increases rates gradually until a "kink" point, then jumps dramatically to discourage over-utilization.

## Blockchain & Smart Contract Terms

### **Smart Contract**
Self-executing code on blockchain that automatically enforces agreements without intermediaries.

### **Upgradeable Contract**
Smart contract designed to allow functionality updates while preserving stored data and user balances.

### **Proxy Contract**
Smart contract that delegates function calls to implementation contracts, enabling upgrades and modular architecture.

### **Multi-Signature (Multi-Sig)**
Security mechanism requiring multiple signatures to execute critical functions, reducing single points of failure.

### **Gas Fee**
Transaction cost paid to blockchain validators to execute smart contract operations.

### **Block**
Unit of blockchain data containing multiple transactions, produced at regular intervals (OORT: ~3 seconds).

### **Web3 Wallet**
Software that manages blockchain private keys and enables interaction with decentralized applications (dApps).

## OORT Network Terms

### **OORT**
Native token of the OORT network used for staking, rewards, and network operations.

### **WOORT (Wrapped OORT)**
ERC-20 compatible version of OORT token used in DeFi applications like InfraFi.

### **OORT Node**
Compute infrastructure device in the OORT network that provides edge computing and AI inference services.

### **Node Staking**
Process of locking OORT tokens to operate a node and earn rewards from network participation.

### **Edge Computing**
Distributed computing paradigm that brings computation closer to data sources and end users.

### **AI Inference**
Process of using trained AI models to make predictions or decisions, often performed on OORT edge nodes.

## Financial Terms

### **Annual Percentage Yield (APY)**
Yearly rate of return including compound interest effects, standardized for comparing investment returns.

### **Total Value Locked (TVL)**
Total dollar value of assets deposited in a DeFi protocol, key metric for protocol success and adoption.

### **Yield**
Return on investment, typically expressed as percentage. In InfraFi, both device rewards and lending interest.

### **Liquidity**
Ease of converting assets to cash. InfraFi unlocks liquidity from typically illiquid infrastructure investments.

### **Capital Efficiency**
Measure of how well capital is utilized to generate returns. InfraFi improves efficiency by enabling borrowing against productive assets.

### **Leverage**
Using borrowed capital to increase investment exposure. InfraFi enables infrastructure operators to leverage existing assets.

## Risk Management Terms

### **Health Factor**
Measure of loan safety, typically calculated as collateral value divided by debt. Higher values indicate safer positions.

### **Liquidation Bonus**
Additional incentive paid to liquidators (typically 5-10%) for executing liquidations and maintaining system health.

### **Slippage**
Difference between expected and actual transaction prices, often due to market volatility or low liquidity.

### **Impermanent Loss**
Temporary loss experienced when token prices change while assets are locked in DeFi protocols.

### **Smart Contract Risk**
Risk of losses due to bugs, vulnerabilities, or exploits in smart contract code.

## Network & Technical Terms

### **Testnet**
Test blockchain network using tokens with no real value, used for development and user education without financial risk.

### **Mainnet**
Primary blockchain network where real transactions occur with tokens having actual economic value.

### **RPC (Remote Procedure Call)**
Communication protocol allowing applications to interact with blockchain networks.

### **Chain ID**
Unique identifier for blockchain networks (e.g., OORT testnet: 970, Ethereum mainnet: 1).

### **Block Explorer**
Web application for viewing blockchain transactions, addresses, and contract interactions (e.g., mainnet-scan.oortech.com).

### **ABI (Application Binary Interface)**
Standard format describing smart contract interfaces, required for applications to interact with contracts.

## Governance Terms

### **DAO (Decentralized Autonomous Organization)**
Organization governed by smart contracts and token holders rather than traditional management structures.

### **Governance Token**
Token that grants holders voting rights on protocol decisions, planned for InfraFi's future decentralization.

### **Proposal**
Formal suggestion for protocol changes submitted to DAO for community voting.

### **Treasury**
Protocol-owned funds used for development, operations, and community initiatives, controlled by governance.

## Economic Model Terms

### **Protocol Fees**
Revenue collected by the protocol from user operations, often shared with token holders or used for development.

### **Tokenomics**
Economic design of token systems, including distribution, utility, incentives, and value capture mechanisms.

### **Network Effects**
Phenomenon where protocol value increases as more users participate, creating competitive advantages.

### **First-Mover Advantage**
Competitive benefit gained by being first to market in a new sector, applicable to InfraFi in DePIN lending.

## Acronyms & Abbreviations

- **APY**: Annual Percentage Yield
- **DAO**: Decentralized Autonomous Organization  
- **DeFi**: Decentralized Finance
- **DePIN**: Decentralized Physical Infrastructure Networks
- **LTV**: Loan-to-Value Ratio
- **NFT**: Non-Fungible Token
- **RPC**: Remote Procedure Call
- **TVL**: Total Value Locked
- **UUPS**: Universal Upgradeable Proxy Standard
- **dApp**: Decentralized Application

## Usage Examples

### **In Context:**
- **"My OORT node has high TVL"** = "My node has significant staked value"
- **"LTV is approaching liquidation threshold"** = "Loan is becoming risky"
- **"Protocol adapter enables multi-chain support"** = "Technical module allows different blockchain integration"
- **"DePIN rewards provide consistent APY"** = "Infrastructure devices generate steady returns"

---

{% hint style="info" %}
**New to these concepts?** Start with [What is InfraFi?](../overview/) for context, then explore specific terms as you encounter them in the documentation.
{% endhint %}

## Quick Reference Cards

<table data-view="cards">
<thead>
<tr>
<th></th>
<th></th>
<th></th>
<th data-hidden data-card-cover data-type="files"></th>
<th data-hidden></th>
<th data-hidden data-card-target data-type="content-ref"></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>DePIN Basics</strong></td>
<td>Physical infrastructure networks</td>
<td>Nodes, rewards, staking</td>
<td></td>
<td></td>
<td><a href="../overview/">overview</a></td>
</tr>
<tr>
<td><strong>DeFi Lending</strong></td>
<td>Borrowing and collateral</td>
<td>LTV, liquidation, interest</td>
<td></td>
<td></td>
<td><a href="../protocol/interest-rates.md">interest-rates.md</a></td>
</tr>
<tr>
<td><strong>Technical Terms</strong></td>
<td>Smart contracts and blockchain</td>
<td>Proxies, adapters, governance</td>
<td></td>
<td></td>
<td><a href="../protocol/architecture.md">architecture.md</a></td>
</tr>
</tbody>
</table>

---

*This glossary is continuously updated. Suggest additions via [GitHub Issues](https://github.com/infrafi/infrafi_documents/issues) or Discord.*
