# Blockchain & Web3 Skill

Smart contracts, DeFi protocols, and blockchain architecture.

## Core Concepts

### Blockchain Types
- **L1 Chains**: Ethereum, Solana, Bitcoin
- **L2 Scaling**: Arbitrum, Optimism, zkSync
- **Sidechains**: Polygon, Avalanche Subnets

### Consensus
- **Proof of Work**: PoW
- **Proof of Stake**: PoS (Ethereum 2.0)
- **Byzantine Fault Tolerance**: PBFT (consortium)

## Smart Contracts

### Solidity (Ethereum)
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.19;

contract SimpleStorage {
    uint256 private value;
    
    event ValueChanged(uint256 newValue);
    
    function set(uint256 _value) public {
        value = _value;
        emit ValueChanged(_value);
    }
    
    function get() public view returns (uint256) {
        return value;
    }
}
```

### Rust (Solana)
```rust
use anchor_lang::prelude::*;

#[program]
pub mod my_program {
    use super::*;
    
    pub fn initialize(ctx: Context<Initialize>) -> Result<()> {
        ctx.accounts.data.value = 0;
        Ok(())
    }
}
```

### Move (Aptos/Sui)
```move
module my_addr::counter {
    struct Counter has key {
        value: u64
    }
    
    public entry fun increment(counter: &mut Counter) {
        counter.value = counter.value + 1;
    }
}
```

## DeFi (Decentralized Finance)

### Core Protocols
| Protocol | Function |
|----------|----------|
| Uniswap | AMM DEX (v2, v3) |
| Aave | Lending/Borrowing |
| Compound | Lending protocol |
| MakerDAO | Stablecoin (DAI) |
| Curve | Stablecoin AMM |
| Lido | Liquid staking |

### DeFi Patterns
- **AMM**: Automated Market Makers
- **Yield Farming**: Liquidity mining
- **Flash Loans**: No-collateral loans (same block)
- **MEV**: Miner/Maximal Extractable Value

### Security Risks
- Reentrancy
- Oracle manipulation
- Sandwich attacks
- Rug pulls
- Infinite mints
- Upgrade risks

## Smart Contract Security

### Tools
- Slither: Static analysis
- Mythril: Symbolic execution
- Echidna: Fuzzing
- Certora: Formal verification
- Tenderly: Debugging

