
[View code on GitHub](https://github.com/solana-labs/solana/tree/master/na/docs/src/api/websocket)

The `websocket` folder in the Solana API contains the implementation of the WebSocket API for real-time communication between clients and the Solana cluster. This API enables developers to subscribe to various events and receive updates as they occur, allowing for efficient and responsive applications.

### Files

1. **`api.md`**: This file contains the documentation for the WebSocket API, detailing the available methods, parameters, and examples of usage. It serves as a reference for developers who want to integrate the WebSocket API into their applications.

2. **`index.md`**: This file serves as an introduction to the WebSocket API, providing a brief overview of its purpose and functionality. It also contains links to the other files in the folder for easy navigation.

### Subfolders

1. **`examples`**: This subfolder contains example code snippets demonstrating how to use the WebSocket API in various scenarios. These examples can serve as a starting point for developers looking to integrate the WebSocket API into their applications.

2. **`methods`**: This subfolder contains detailed documentation for each of the available WebSocket API methods. Each method is documented in a separate file, providing information on the method's purpose, parameters, and usage examples.

### Usage

The WebSocket API allows developers to subscribe to various events on the Solana cluster, such as account updates, program logs, and slot updates. By subscribing to these events, applications can receive real-time updates and respond accordingly.

For example, to subscribe to account updates, you can use the `accountSubscribe` method:

```javascript
const solanaWeb3 = require('@solana/web3.js');
const connection = new solanaWeb3.Connection('https://api.mainnet-beta.solana.com');

const accountToSubscribe = new solanaWeb3.PublicKey('exampleAccountPublicKey');

connection.onAccountChange(accountToSubscribe, (accountInfo) => {
  console.log('Account data:', accountInfo.data);
});
```

This code snippet creates a connection to the Solana cluster and subscribes to updates for a specific account. Whenever the account data changes, the provided callback function will be executed, logging the updated account data.

Similarly, you can subscribe to program logs using the `logsSubscribe` method:

```javascript
const solanaWeb3 = require('@solana/web3.js');
const connection = new solanaWeb3.Connection('https://api.mainnet-beta.solana.com');

const programToSubscribe = new solanaWeb3.PublicKey('exampleProgramPublicKey');

connection.onProgramLog(programToSubscribe, (logMessage) => {
  console.log('Log message:', logMessage);
});
```

In this example, the application subscribes to log messages generated by a specific program. Whenever a log message is generated, the provided callback function will be executed, logging the message.

Overall, the WebSocket API provides a powerful and efficient way for developers to build responsive applications that interact with the Solana cluster in real-time. By subscribing to relevant events, applications can stay up-to-date with the latest changes and provide a seamless user experience.