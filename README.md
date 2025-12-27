# Hitvamp Vault Integration Project

This repository contains a full-stack blockchain integration project for interacting with Hitvamp vaults. It includes smart contracts, deployment scripts, and a modern frontend for user interaction.

## Project Structure

```
frontend/        # Next.js frontend application
Hitvamp/          # Solidity smart contracts and Foundry tests
```

### Frontend
- Built with Next.js and TypeScript
- Located in the `frontend/` directory
- Contains UI components for wallet connection, deposit, withdrawal, and dashboard
- Uses modern React patterns and hooks

### Smart Contracts
- Located in the `Hitvamp/` directory
- Written in Solidity
- Includes contracts for vault locking, yield management, and interfaces
- Uses Foundry for testing and deployment

#### Key Contracts
- `fixedLockVault.sol`: Main vault contract
- `HitvampLock.sol`: Handles Hitvamp-specific locking logic
- `yieldLockManager.sol`: Manages yield and lock operations
- `interfaces/`: ERC20 and router interfaces
- `libraries/`: Helper libraries

#### Scripts
- `scripts/deploy.s.sol`: Deployment script for Foundry

#### Tests
- `test/unit/`: Unit tests for contracts
- `test/integration/`: Integration tests for contract flows

## Getting Started

### Prerequisites
- Node.js (for frontend)
- Foundry (for Solidity development)
- Git

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repo-url>
   cd <repo-root>
   ```

2. **Install frontend dependencies:**
   ```bash
   cd frontend
   npm install
   ```

3. **Install Foundry:**
   Follow instructions at [Foundry Book](https://book.getfoundry.sh/getting-started/installation)

### Running the Frontend
```bash
cd frontend
npm run dev
```
The app will be available at `http://localhost:3000`.

### Running Tests
```bash
cd Hitvamp
forge test
```

### Deploying Contracts
Edit `scripts/deploy.s.sol` as needed, then run:
```bash
forge script scripts/deploy.s.sol --broadcast --rpc-url <YOUR_RPC_URL>
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](LICENSE)
