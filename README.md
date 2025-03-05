# Bridge an ERC-20 Token 

## Overview
This project bridges and claims assets through a two-step process. First, an asset is bridged, then it is claimed.

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/AkshatGada/Bridge_ERC20_tutorial.git example 
   cd example 
   ```
2. **Install Packages**
   ```bash
   npm install 
   ```
3. **Configure Environment Variables**
   - Create a `.env` file in the root directory.
   - Use the `.env.example` file as a template.
   - Fill in the required details in your new `.env` file.

4. **Bridge the Asset**
   - Run the following command:
     ```bash
     node bridge_asset.js
     ```
5. **Claim the Asset**
   - Once the transaction is **BRIDGED**, run:
     ```bash
     node claim_asset.js
     ```
   - The transaction state will then change to **CLAIMED**.

## Transaction State Changes

| Step          | Command/Action           | Transaction State |
|---------------|--------------------------|-------------------|
| Bridge Asset  | `node bridge_asset.js`   | BRIDGED           |
| Transition    | *(Automatic Process)*    | READY_TO_CLAIM    |
| Claim Asset   | `node claim_asset.js`    | CLAIMED           |