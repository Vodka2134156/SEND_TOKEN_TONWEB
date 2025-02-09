# Jetton Transfer Script for TON Blockchain

This script allows you to **send Jettons (TON tokens)** from a **V3R2 TON wallet** to a recipient's address using a **mnemonic-based wallet**.

## Features
- 🏦 **Initialize a Wallet V3R2** using a **mnemonic phrase**.
- 🔄 **Retrieve the Jetton wallet address** linked to the sender.
- 💸 **Transfer Jettons to a recipient's address** with a specified amount.
- ✅ **Uses the TON API & TON SDK** for interacting with the blockchain.

---

## 🛠️ Setup & Installation

### 1️⃣ Install Dependencies
Make sure you have **Node.js** installed, then install the required packages:

```sh
npm install tonweb tonweb-mnemonic @ton/ton @orbs-network/ton-access
```

### 2️⃣ Configure the Script
Before running the script, modify these values:

- **Token Contract Address** (`token_address`)
- **Recipient Address** (`recipient_address`)
- **Amount of Jettons to Send** (`amount`)
- **Mnemonic Array** (`mnemonic_array` - your 24-word seed phrase)

Example:
```javascript
const token_address = "EQCIiZ6b5fYSHLfCCAqi4KsIeqQAD3H_HSP-V5r4OUgTEuAs";
const recipient_address = "UQAisQIXtyaEfWfXyIMOAffNoKDLnUgejb1XdLNFH7mNDTVq";
const amount = "500"; // Amount in basic units
const mnemonic_array = ["word1", "word2", "word3", "...", "word24"];
```

### 3️⃣ Run the Script
Execute the script using Node.js:
```sh
node transfer.js
```

---

## 📝 How It Works

1. **Loads your mnemonic phrase** and derives the **wallet's public/private keys**.
2. **Initializes a Wallet V3R2** (standard TON wallet version 3, revision 2).
3. **Finds the Jetton Wallet Address** associated with your wallet.
4. **Sends the specified Jetton amount** to the recipient.
5. **Waits for blockchain confirmation** and prints the transaction status.

---

## 🚀 Example Output
```sh
Current seqno: 5
Transaction executed successfully!
```

If there's an error, it will display the issue.

---

## ⚠️ Security Notice
🔑 **DO NOT share your mnemonic phrase!** Your **24-word seed** controls your funds.

- Consider using a **secure environment** to run this script.
- Ensure you **double-check recipient addresses** before sending Jettons.
- Use **testnet** for testing before sending on **mainnet**.

---

## 📖 Additional Resources
- [TON API Documentation](https://ton.org/docs/)
- [Jetton Standard]([https://github.com/ton-blockchain/TEPs/blob/master/text/0074-jettons.md](https://github.com/EmelyanenkoK/modern_jetton))

---

## 💡 Need Help?
If you encounter any issues, feel free to ask for help in the **TON Developer Community** or open an issue.

---

### 🎉 Happy Hacking on TON! 🚀

