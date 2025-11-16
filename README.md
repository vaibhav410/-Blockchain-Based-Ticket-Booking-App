# Blockchain-Based-Ticket-Booking-App
A decentralized, multi modal ticket booking platform built on the Ethereum blockchain. This project ensures transparent, fraud proof ticket transactions for railways, flights, buses, and cabs.

# 🌟 About The Project
<img width="1545" alt="Dashboard Preview" src="https://github.com/user-attachments/assets/c59f859d-8655-4054-8187-dc63390b420d" />
Traditional ticket booking systems are centralized and vulnerable to fraud, scalping, and unauthorized reselling. Our blockchain-based solution provides:

# 🔒 Security: Immutable records on Ethereum blockchain

🎯 **Transparency**: All transactions are publicly verifiable

⚡ **Efficiency**: No intermediaries, direct peer to peer transactions

🛡️ **Anti-Fraud**: Cryptographic proof of ownership

# Supported Services

🚂 **Railway Tickets**

✈️ **Flight Bookings**

🚌 **Bus Reservations**

🚕 **Cab Services**

# ✨ Features
## Core Functionality
✅ **Smart Contract Based Ticketing** - Automated ticket creation and ownership transfer

✅ **Wallet Authentication** - Secure login via MetaMask or other Web3 wallets

✅ **Real-time Verification** - Instant ticket validation on the blockchain

✅ **Ownership Tracking** - Complete history of ticket ownership

✅ **Fraud Prevention** - Duplicate tickets impossible due to blockchain uniqueness

✅ **Decentralized Storage** - No single point of failure

# User Features
🔍 Search and filter tickets by service type

💳 Book tickets using Ethereum (ETH)

📱 Responsive design for mobile and desktop

🎫 Generate QR codes for easy verification

📊 View booking history

💰 Transparent pricing with no hidden fees

# 🛠️ Tech Stack
## Frontend
**HTML5** - Structure and content

**CSS3** - Styling and animations

**JavaScript (ES6+)** - Interactive functionality

**Web3.js** - Ethereum blockchain interaction

# Blockchain
**Solidity** - Smart contract development

**Ethereum** - Blockchain platform

**Truffle Suite** - Development framework

**Ganache** - Local blockchain for testing

# Tools & Libraries
**MetaMask** - Wallet integration

**OpenZeppelin** - Secure smart contract libraries

 

## 🎥 Demo
Watch the demo video here: [Demo Video Link] (https://drive.google.com/file/d/1N_55kPtRz87Sxk6C409R7XMt4MNjAe1d/view?usp=drive_link)

Installation
1️⃣ Clone the Repository
Bash
``git clone https://github.com/yourusername/blockchain-ticket-app.git
cd blockchain-ticket-app
``

2️⃣ Install Dependencies
Bash
``npm install
``

3️⃣ Setup Ganache

Open Ganache and create a new workspace

Set RPC Server to HTTP://127.0.0.1:7545

Note down the mnemonic phrase

4️⃣ Configure MetaMask
Install MetaMask browser extension

Import accounts using Ganache mnemonic

Connect to localhost:7545 network

5️⃣ Compile Smart Contracts
Bash
``truffle compile
``

6️⃣ Deploy to Local Blockchain
Bash
``truffle migrate --reset
``

7️⃣ Run Tests (Optional)
Bash
``truffle test
``

8️⃣ Start the Frontend
Bash
``npm start
``

### or simply open index.html in your browser

📖 Usage
Booking a Ticket

Connect Wallet

Click "Connect Wallet" button

Approve MetaMask connection

Select Service

Choose from Railway, Flight, Bus, or Cab

Enter Details

Fill in travel information (origin, destination, date)

Review pricing

Confirm Transaction

Approve transaction in MetaMask

Wait for blockchain confirmation

Receive Ticket

Get unique ticket ID and QR code

Ticket is stored on blockchain

Verifying a Ticket


JavaScript

// Check ticket validity
const isValid = await ticketContract.verifyTicket(ticketId);
📜 Smart Contract
Main Contract: TicketBooking.sol
solidity

// Simplified structure
contract TicketBooking {
    struct Ticket {
        uint256 id;
        address owner;
        string serviceType;
        string origin;
        string destination;
        uint256 price;
        uint256 timestamp;
        bool isValid;
    }
    
    mapping(uint256 => Ticket) public tickets;
    
    function bookTicket(...) public payable { }
    function transferTicket(...) public { }
    function verifyTicket(...) public view returns (bool) { }
    function cancelTicket(...) public { }
}
Key Functions

Function	Description	Access

bookTicket()-	Create a new ticket	Public (Payable)

verifyTicket()-	Check ticket validity	Public (View)

transferTicket()-	Transfer ownership	Owner Only

cancelTicket()-	Cancel and refund	Owner Only


