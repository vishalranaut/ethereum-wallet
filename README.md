# Ethereum Test Wallet

A simple Ethereum web wallet built with Node.js and React for educational purposes. This project demonstrates the fundamentals of blockchain wallet functionality in a clean, interactive interface.

> **⚠️ IMPORTANT**: This wallet is for learning purposes only. Do not use it in production environments or with real Ethereum accounts containing actual funds.

## Features

- Connect to the Ethereum Ropsten test network
- Generate and manage Ethereum test accounts
- View account balances and transaction history
- Send and receive test Ether
- Monitor real-time updates of your wallet activity

## Prerequisites

Before you begin, you'll need:

- [Node.js](https://nodejs.org/) (v14+ recommended)
- npm or yarn package manager
- Free API keys from:
  - [Infura](https://infura.io/) - For Ethereum network connectivity
  - [Etherscan](https://etherscan.io/) - For fetching balance and transaction data

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ethereum-test-wallet.git
   cd ethereum-test-wallet
   ```

2. Install dependencies:
   ```bash
   npm install
   ```
   or with yarn:
   ```bash
   yarn install
   ```

3. Configure environment variables:
   ```bash
   cp .env.sample .env
   ```

4. Open the `.env` file and set the following variables:

   | Variable | Description | Example |
   |----------|-------------|---------|
   | `ETHERSCAN_API_KEY` | Your Etherscan API key | abc123... |
   | `INFURA_API_KEY` | Your Infura API key | xyz789... |
   | `REACT_APP_BACKEND_HOST` | Domain or IP of server side app | http://localhost |
   | `REACT_APP_BACKEND_PORT` | Port of server side app | 3001 |
   | `PORT` | Port of client side app | 3002 |
   | `REACT_APP_UPDATE_INTERVAL` | Refresh interval (ms) for balance/transactions | 15000 |

## Running the Application

1. Start the server:
   ```bash
   node server.js
   ```

2. In a new terminal window, start the client:
   ```bash
   npm start
   ```
   or with yarn:
   ```bash
   yarn start
   ```

3. Access the wallet in your browser at `http://localhost:3002`

## Getting Test Ether

To experiment with the wallet, you'll need test Ether. You can obtain it for free from:
- [Ropsten Faucet](https://faucet.ropsten.be/)
- [Ropsten Testnet Faucet](https://faucet.dimensions.network/)

## Project Structure

```
ethereum-test-wallet/
├── server.js          # Backend Node.js server
├── src/
│   ├── App.js         # Main React component
│   ├── components/    # React UI components
│   ├── services/      # API and blockchain services
│   └── utils/         # Helper functions
├── public/            # Static assets
└── .env               # Environment configuration
```

## Security Notes

- This application is not audited for security
- Private keys are stored in browser localStorage (not secure for production)
- No encryption is implemented for sensitive data

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
