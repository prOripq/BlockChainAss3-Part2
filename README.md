# Aitu_SE2315_YussupovZhangir Smart Contract

## 📌 Project Overview
This repository contains a Solidity smart contract, **Aitu_SE2315_YussupovZhangir**, implemented using OpenZeppelin's ERC20 and ERC20Permit standards. The contract allows token minting, transaction tracking, and timestamp retrieval.

## 🛠 Features
- Implements ERC20 and ERC20Permit.
- Supports token minting with an initial supply parameter.
- Functions for transaction sender, receiver, and timestamp retrieval.

## 📂 File Structure
```
📁 hardhat-project
 ├── 📂 contracts
 │   └── Token.sol    # Smart contract
 ├── 📂 test
 │   └── Token.js     # Hardhat test script
 │   └── TokenModified.js   # Hardhat modified test script
 ├── 📜 hardhat.config.js  # Hardhat configuration
 ├── 📜 package.json  # Dependencies
 ├── 📜 package-lock.json     # Data
```

## 🚀 Deployment & Testing

### 1️⃣ Install Dependencies
Run the following command to install required dependencies:
```sh
npm install
```

### 2️⃣ Compile the Smart Contract
```sh
npx hardhat compile
```

### 3️⃣ Run Test Cases
Execute the Hardhat test script:
```sh
npx hardhat test
```

## 📜 Smart Contract Functions
### 1️⃣ `constructor(uint256 initialSupply)`
- Deploys the contract and mints `initialSupply` tokens to the deployer.

### 2️⃣ `getTransactionSender()`
- Returns the sender of the current transaction.

### 3️⃣ `getTransactionReceiver(address _to)`
- Returns the given address `_to`.

### 4️⃣ `getLatestTransactionTimestamp()`
- Retrieves the timestamp of the latest transaction.

## 🏗 Usage
To interact with the deployed contract, use the Hardhat console:

### 1️⃣ Deploy the Contract
```sh
npx hardhat run scripts/deploy.js --network localhost
```

### 2️⃣ Mint Tokens
```js
const [owner] = await ethers.getSigners();
const balance = await token.balanceOf(owner.address);
console.log(`Owner balance: ${ethers.utils.formatUnits(balance, 18)} MTK`);
```

### 3️⃣ Check Sender Address
```js
const sender = await token.getTransactionSender();
console.log(`Transaction sender: ${sender}`);
```

### 4️⃣ Check Receiver Address
```js
const receiver = await token.getTransactionReceiver("0xYourAddress");
console.log(`Transaction receiver: ${receiver}`);
```

### 5️⃣ Retrieve Latest Timestamp
```js
const timestamp = await token.getLatestTransactionTimestamp();
console.log(`Latest transaction timestamp: ${timestamp}`);
```




## Demo Screenshots
![image](https://github.com/user-attachments/assets/20955b8f-9426-402f-910e-6c872185b424)
![image](https://github.com/user-attachments/assets/680c0402-7847-4480-a61a-eab4646536e2)
![image](https://github.com/user-attachments/assets/e2f2b04c-4909-4bcb-ad30-3ac6a7e2fcbe)
![image](https://github.com/user-attachments/assets/02004507-d9e9-4ffb-a228-e40485fcbce0)


## 📤 Examples
1. **Initialize the smart contract**
   ```js
   npx hardhat compile;
   ```
2. **Start to test it:**
   ```js
   npx hardhat test;
   ```

## 📄 License
This project is licensed under the **MIT License**.

## 🔗 References
- [Hardhat Documentation](https://hardhat.org/)
- [OpenZeppelin Contracts](https://github.com/OpenZeppelin/openzeppelin-contracts)
