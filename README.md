# Avalanche User Registry

A decentralized user registry built on the Avalanche blockchain with a beautiful, modern frontend. This project allows users to register their digital identity, get verified, and build reputation on-chain.

## Features

### Smart Contract Features
- **User Registration**: Register with username, email, IPFS profile hash, and tags
- **Verification System**: Request and approve user verification
- **Reputation Management**: Build and manage on-chain reputation
- **Fee System**: Configurable registration and verification fees
- **Upgradeable**: Built with OpenZeppelin upgrades for future improvements
- **Access Control**: Owner and verifier role management

### Frontend Features
- **Wallet Connection**: Support for MetaMask, WalletConnect, and other wallets
- **Beautiful UI**: AVAX-themed design with modern aesthetics
- **User Registration Form**: Complete registration workflow
- **Registry View**: Browse and search registered users
- **Responsive Design**: Works on desktop and mobile devices

## Tech Stack

- **Smart Contract**: Solidity 0.8.20, OpenZeppelin Contracts
- **Frontend**: React 18, Ethers.js 5.7.2, Web3Modal
- **Development**: Hardhat, Node.js
- **Blockchain**: Avalanche C-Chain

## Quick Start

### Prerequisites
- Node.js 16+ 
- npm or yarn
- MetaMask or other Web3 wallet
- AVAX testnet tokens (for testing)

### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd user-registry
```

2. **Install dependencies**
```bash
# Install smart contract dependencies
npm install

# Install frontend dependencies
cd frontend
npm install --legacy-peer-deps
cd ..
```

3. **Environment Setup**
```bash
# Copy environment file
cp env.example .env

# Edit .env with your configuration
PRIVATE_KEY=your_private_key_here
SNOWTRACE_API_KEY=your_snowtrace_api_key_here
```

### Smart Contract Deployment

1. **Compile contracts**
```bash
npx hardhat compile
```

2. **Deploy to Fuji testnet**
```bash
npx hardhat run scripts/deploy.js --network fuji
```

3. **Update contract address**
After deployment, update the `CONTRACT_ADDRESS` in `frontend/src/App.js` with the deployed contract address.

### Frontend Development

1. **Start the development server**
```bash
cd frontend
npm start
```

2. **Open your browser**
Navigate to [http://localhost:3000](http://localhost:3000)

## Usage

### For Users

1. **Connect Wallet**: Click "Connect Wallet" and approve the connection
2. **Register**: Fill out the registration form with your details
3. **Pay Fee**: Confirm the transaction to pay the registration fee
4. **Get Verified**: Request verification from authorized verifiers
5. **Build Reputation**: Earn reputation points through community interactions

### For Verifiers

1. **Get Authorized**: Contact the contract owner to become a verifier
2. **Review Requests**: Approve or reject verification requests
3. **Manage Reputation**: Award or deduct reputation points from users

### For Developers

1. **Deploy Contract**: Use the deployment script to deploy to your preferred network
2. **Customize Frontend**: Modify the React components to match your needs
3. **Add Features**: Extend the smart contract with additional functionality

## Smart Contract Functions

### User Functions
- `registerUser(username, email, profileHash, tags)` - Register a new user
- `updateProfile(profileHash, tags)` - Update user profile
- `requestVerification(documentHash)` - Request verification

### Verifier Functions
- `approveVerification(requestId)` - Approve verification request
- `rejectVerification(requestId, reason)` - Reject verification request
- `updateReputation(user, reputationChange)` - Update user reputation

### Admin Functions
- `addVerifier(verifier)` - Add new verifier
- `removeVerifier(verifier)` - Remove verifier
- `updateFees(registrationFee, verificationFee)` - Update fees
- `withdrawFees()` - Withdraw accumulated fees

## Network Configuration

### Fuji Testnet
- **RPC URL**: https://api.avax-test.network/ext/bc/C/rpc
- **Chain ID**: 43113
- **Explorer**: https://testnet.snowtrace.io

### Mainnet
- **RPC URL**: https://api.avax.network/ext/bc/C/rpc
- **Chain ID**: 43114
- **Explorer**: https://snowtrace.io

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support and questions:
- Create an issue on GitHub
- Join our Discord community
- Check the documentation

## Roadmap

- [ ] IPFS integration for profile storage
- [ ] Advanced reputation algorithms
- [ ] Social features and connections
- [ ] Mobile app development
- [ ] Cross-chain compatibility
- [ ] DAO governance integration

---

Built with ❤️ for the Avalanche ecosystem 
