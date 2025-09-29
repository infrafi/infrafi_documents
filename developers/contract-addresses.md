---
icon: map-pin
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

# Contract Addresses

Official InfraFi Protocol contract addresses for all supported networks.

{% hint style="danger" %}
**Verify Addresses**: Always verify contract addresses from official sources before interacting. Never trust addresses from unofficial sources.
{% endhint %}

## OORT Testnet (Chain ID: 970)

### Core InfraFi Contracts

| Contract | Address | Description |
|----------|---------|-------------|
| **NodeVaultUpgradeable** | `0x74f68Eec49DFAd34E22f3f6F3e38d4d92D8ab676` | Main vault and lending contract |
| **ProtocolAdapterRegistry** | `0xC3305D14cbE9d1bE5BF9E601085525bB4a491a96` | Multi-protocol adapter coordinator |
| **NodeProxyManager** | `0xAd85e8Ac6be7323D720332428AbAdC235442d825` | Proxy contract manager |
| **OortProtocolAdapter** | `0xE2c3d808B6FCEC0bCda60DC1f612D83fD6265E8f` | OORT network integration |

### External OORT Contracts

| Contract | Address | Description |
|----------|---------|-------------|
| **OORT Node Contract** | `0xA97E5185DC116588A85197f446Aa87cE558d254C` | OORT network node registry |
| **OORT Device Contract** | `0x7b6Fd29a1A37DfeAB02704366B2AfD3adE2af974` | OORT device management |
| **WOORT Token** | `0x0809f1dC272F42F96F0B06cE5fFCEC97cB9FA82d` | Wrapped OORT token |

### Network Information

```json
{
  "networkName": "OORT Testnet",
  "chainId": 970,
  "rpcUrl": "https://mainnet-rpc.oortech.com",
  "blockExplorerUrl": "https://mainnet-scan.oortech.com",
  "nativeCurrency": {
    "name": "OORT",
    "symbol": "OORT", 
    "decimals": 18
  }
}
```

## OORT Mainnet (Planned Q1 2025)

{% hint style="info" %}
**Coming Soon**: Mainnet deployment planned for Q1 2025 after security audit completion.
{% endhint %}

### Planned Mainnet Configuration

| Contract | Status | Notes |
|----------|--------|-------|
| **NodeVaultUpgradeable** | 🔄 Pending | Conservative parameters for launch |
| **ProtocolAdapterRegistry** | 🔄 Pending | Same codebase as testnet |
| **NodeProxyManager** | 🔄 Pending | Production-ready version |
| **OortProtocolAdapter** | 🔄 Pending | Mainnet OORT contract integration |

### Mainnet Network Info

```json
{
  "networkName": "OORT Mainnet", 
  "chainId": 970,
  "rpcUrl": "https://mainnet-rpc.oortech.com",
  "blockExplorerUrl": "https://mainnet-scan.oortech.com",
  "nativeCurrency": {
    "name": "OORT",
    "symbol": "OORT",
    "decimals": 18
  }
}
```

## Contract ABIs

### Quick Integration

For rapid integration, use these ABI endpoints:

```javascript
// Testnet ABI endpoints
const VAULT_ABI_URL = "https://api.infrafi.com/abi/testnet/vault";
const ADAPTER_ABI_URL = "https://api.infrafi.com/abi/testnet/adapter";

// Load ABIs
const vaultABI = await fetch(VAULT_ABI_URL).then(r => r.json());
const adapterABI = await fetch(ADAPTER_ABI_URL).then(r => r.json());
```

### Key Interfaces

#### **NodeVault Interface**
```solidity
interface INodeVault {
    // Core operations
    function depositNodes(uint256[] calldata nodeIds, uint256[] calldata nodeTypes) external;
    function borrow(uint256 amount) external;
    function repay(uint256 amount) external;
    function withdrawNodes(uint256[] calldata nodeIds, uint256[] calldata nodeTypes) external;
    
    // View functions
    function getUserHealth(address user) external view returns (uint256, uint256, uint256, bool);
    function getNodeInfo(uint256 nodeId, uint256 nodeType) external view returns (...);
    function getUserDebt(address user) external view returns (uint256);
}
```

#### **Protocol Adapter Interface**
```solidity
interface IProtocolAdapter {
    function getProtocolInfo() external view returns (ProtocolInfo memory);
    function getNodeValue(uint256 nodeId) external view returns (NodeValue memory);
    function getDepositSteps(uint256 nodeId, address currentOwner, address targetOwner) 
        external view returns (DepositStep[] memory);
    function getWithdrawalSteps(uint256 nodeId, address currentOwner, address targetOwner)
        external view returns (WithdrawalStep[] memory);
}
```

## Environment Variables

### For Development

```bash
# OORT Testnet Environment Variables
OORT_TESTNET_RPC_URL=https://mainnet-rpc.oortech.com
OORT_TESTNET_CHAIN_ID=970
OORT_TESTNET_EXPLORER=https://mainnet-scan.oortech.com

# InfraFi Testnet Contracts
OORT_TESTNET_VAULT_CONTRACT=0x74f68Eec49DFAd34E22f3f6F3e38d4d92D8ab676
OORT_TESTNET_PROTOCOL_ADAPTER_REGISTRY=0xC3305D14cbE9d1bE5BF9E601085525bB4a491a96
OORT_TESTNET_NODE_PROXY_MANAGER=0xAd85e8Ac6be7323D720332428AbAdC235442d825
OORT_TESTNET_PROTOCOL_ADAPTER=0xE2c3d808B6FCEC0bCda60DC1f612D83fD6265E8f

# External OORT Contracts
OORT_TESTNET_NODE_CONTRACT=0xA97E5185DC116588A85197f446Aa87cE558d254C
OORT_TESTNET_DEVICE_CONTRACT=0x7b6Fd29a1A37DfeAB02704366B2AfD3adE2af974
OORT_TESTNET_WOORT_CONTRACT=0x0809f1dC272F42F96F0B06cE5fFCEC97cB9FA82d
```

### For Production (Future)

```bash
# OORT Mainnet Environment Variables (Planned)
OORT_MAINNET_RPC_URL=https://mainnet-rpc.oortech.com
OORT_MAINNET_CHAIN_ID=970
OORT_MAINNET_EXPLORER=https://mainnet-scan.oortech.com

# InfraFi Mainnet Contracts (TBD)
OORT_MAINNET_VAULT_CONTRACT=[TO_BE_ANNOUNCED]
OORT_MAINNET_PROTOCOL_ADAPTER_REGISTRY=[TO_BE_ANNOUNCED]
# ... (additional addresses to be announced)

# External OORT Mainnet Contracts
OORT_MAINNET_NODE_CONTRACT=0xDE155823964816d6E67de8eA31DEf95D59aaE2Fb
OORT_MAINNET_DEVICE_CONTRACT=0xdFfe6151e33E0De4f5658dCd28454E7372CD20Ad
OORT_MAINNET_WOORT_CONTRACT=0xEAd29460881f38ADA079A38ac3D82E2D088930d9
```

## Security Verification

### Contract Verification

#### **Testnet Verification Status**
| Contract | Verified | Explorer Link |
|----------|----------|---------------|
| **NodeVaultUpgradeable** | ✅ | [View on Explorer](https://mainnet-scan.oortech.com/address/0x74f68Eec49DFAd34E22f3f6F3e38d4d92D8ab676) |
| **ProtocolAdapterRegistry** | ✅ | [View on Explorer](https://mainnet-scan.oortech.com/address/0xC3305D14cbE9d1bE5BF9E601085525bB4a491a96) |
| **NodeProxyManager** | ✅ | [View on Explorer](https://mainnet-scan.oortech.com/address/0xAd85e8Ac6be7323D720332428AbAdC235442d825) |
| **OortProtocolAdapter** | ✅ | [View on Explorer](https://mainnet-scan.oortech.com/address/0xE2c3d808B6FCEC0bCda60DC1f612D83fD6265E8f) |

#### **Verification Commands**
```bash
# Verify contract on OORT Explorer
npx hardhat verify --network oort_testnet [CONTRACT_ADDRESS] [CONSTRUCTOR_ARGS]

# Example: Verify vault contract
npx hardhat verify --network oort_testnet \
  0x74f68Eec49DFAd34E22f3f6F3e38d4d92D8ab676 \
  "0x0809f1dC272F42F96F0B06cE5fFCEC97cB9FA82d" \
  "0xC3305D14cbE9d1bE5BF9E601085525bB4a491a96" \
  # ... additional constructor arguments
```

## Usage Examples

### Web3.js Integration

```javascript
const Web3 = require('web3');

// Connect to OORT testnet
const web3 = new Web3('https://mainnet-rpc.oortech.com');

// Contract addresses
const VAULT_ADDRESS = '0x74f68Eec49DFAd34E22f3f6F3e38d4d92D8ab676';
const WOORT_ADDRESS = '0x0809f1dC272F42F96F0B06cE5fFCEC97cB9FA82d';

// Initialize contracts
const vaultContract = new web3.eth.Contract(VAULT_ABI, VAULT_ADDRESS);
const woortContract = new web3.eth.Contract(ERC20_ABI, WOORT_ADDRESS);

// Example: Check user's debt
const userDebt = await vaultContract.methods.getUserDebt(userAddress).call();
console.log(`User debt: ${web3.utils.fromWei(userDebt, 'ether')} WOORT`);
```

### Ethers.js Integration

```javascript
const { ethers } = require('ethers');

// Provider setup
const provider = new ethers.providers.JsonRpcProvider(
  'https://mainnet-rpc.oortech.com'
);

// Contract instances
const vault = new ethers.Contract(VAULT_ADDRESS, VAULT_ABI, provider);
const woort = new ethers.Contract(WOORT_ADDRESS, ERC20_ABI, provider);

// Example: Get protocol statistics
async function getProtocolStats() {
  const totalSupply = await vault.totalSupply();
  const totalBorrows = await vault.totalBorrows();
  const utilizationRate = totalBorrows.mul(10000).div(totalSupply);
  
  return {
    totalSupply: ethers.utils.formatEther(totalSupply),
    totalBorrows: ethers.utils.formatEther(totalBorrows),
    utilizationRate: utilizationRate.toNumber() / 100 // Convert to percentage
  };
}
```

## Multi-Chain Future

### Planned Network Support

| Network | Timeline | Purpose |
|---------|----------|---------|
| **Ethereum Mainnet** | Q3 2025 | Maximum security and liquidity |
| **Polygon** | Q4 2025 | Lower gas costs |
| **Arbitrum** | Q4 2025 | Layer 2 scaling |
| **Additional Networks** | 2026+ | Community-driven expansion |

### Cross-Chain Architecture
Future multi-chain deployment will use:
- **Unified Liquidity**: Cross-chain bridges for token movement
- **Shared State**: Synchronized collateral and debt tracking
- **Local Execution**: Network-specific optimizations

## Support & Updates

### Getting Updates
- **GitHub Releases**: [InfraFi Releases](https://github.com/infrafi/infrafi_contracts/releases)
- **Discord Announcements**: Real-time deployment updates
- **Documentation**: Always check this page for latest addresses

### Reporting Issues
- **Wrong Address**: Report immediately via Discord #security
- **Integration Problems**: GitHub issues with detailed reproduction steps  
- **Security Concerns**: Direct contact via security@infrafi.com

---

{% hint style="warning" %}
**Always Verify**: Contract addresses can change during development. Always verify against official sources before integration.
{% endhint %}

## Related Resources

- **[Integration Guide](integration-guide.md)** - How to build on InfraFi
- **[API Reference](api-reference.md)** - Complete interface documentation
- **[Testing Guide](testing.md)** - Development and testing setup
