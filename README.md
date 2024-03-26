# Tea Protocol Smart Contract Library

The **Tea Protocol Smart Contract Library** provides a set of utilities for interacting with smart contracts related to tea production, supply chain, and quality assurance. Whether you're building a decentralized application (DApp) for tea enthusiasts or integrating tea-related functionality into an existing project, this library simplifies the process.

## Features

- **Create Tea Batches**: Easily create new tea batches on the blockchain.
- **Retrieve Tea Batch Details**: Retrieve information about a specific tea batch.
- **Interact with Smart Contracts**: Connect to Ethereum-compatible networks and interact with deployed smart contracts.

## Installation

Install the library using npm:

```bash
npm install my-smart-contract-library
```

## Usage

```javascript
const Web3 = require('web3');
const TeaProtocol = require('my-smart-contract-library');

// Initialize Web3 with your preferred provider (e.g., Infura, local Ganache)
const web3 = new Web3('https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID');

// Instantiate TeaProtocol with the contract address
const contractAddress = '0xYourContractAddress';
const teaProtocol = new TeaProtocol(web3, contractAddress);

// Example: Create a new tea batch
async function createTeaBatch() {
    try {
        const batchId = '123';
        const teaType = 'Green Tea';
        const quantity = 100; // In kilograms

        await teaProtocol.createTeaBatch(batchId, teaType, quantity);
        console.log(`Tea batch ${batchId} created successfully.`);
    } catch (error) {
        console.error('Error creating tea batch:', error.message);
    }
}

// Example: Get tea batch details
async function getTeaBatchDetails(batchId) {
    try {
        const result = await teaProtocol.getTeaBatch(batchId);
        console.log('Tea batch details:', result);
    } catch (error) {
        console.error('Error retrieving tea batch details:', error.message);
    }
}

// Call your functions here
createTeaBatch();
getTeaBatchDetails('123');
```

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

