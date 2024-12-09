# Adv-Blockchain-Final-Project
# Decentralized Crowdfunding Platform

Team Members:
•	Kuldeep Singh Rathore : kuldeepsingh@csu.fullerton.edu
•	Mohit Patni : mohitpatni@csu.fullerton.edu 

Project Overview:
This project is a Decentralized Crowdfunding Platform built on Ethereum smart contracts, using Solidity, Truffle, and a React.js frontend with Web3 integration. 
It allows creators to:
•	Create crowdfunding projects with funding goals and deadlines.
•	Receive contributions from backers.
•	Withdraw funds if the funding goal is met and approved by trusted signers.
  Backers can:
•	Contribute to projects in USD terms (converted to ETH at a fixed, hardcoded rate).
•	Leave a comment along with their contribution.
•	Be recognized as a top donor if their contribution is among the highest.


Feature we have implemented:

1.	User Registration: Users can register a readable name on-chain instead of relying solely on Ethereum addresses. 
2.	ETH-to-USD Conversion: Projects display funding goals and contributions in USD using a fixed ETH/USD rate to simplify demonstrations. 
3.	Project Creation & Management: Users create projects with a title, description, funding goal (USD), and a strict deadline. Validation ensures deadlines are in the future. 
4.	Funding with Comments: Contributors can fund projects and store an on-chain comment, adding personality and context to their contributions. 
5.	Top Donors Section: Displays the top 3 donors per project, including their chosen names, amounts (in USD), and comments, encouraging user engagement and transparency. 
6.	Referral System: Users can share referral links. Successful referrals award referral counts and points, which can be claimed as rewards. 
7.	Multi-Signature Approvals for Withdrawals: Implemented a secure withdrawal mechanism requiring approval from trusted signers, preventing unauthorized fund releases. 
8.	Real-Time UI Updates: On-chain events (project creation, funding, withdrawals) dynamically update the frontend without manual refresh. 
9.	Comment Display: Comments are stored on-chain and displayed per contribution, building trust and narrative around projects. 
10.	Micropayment Channel (Conceptual): Showcases how off-chain signed messages can facilitate efficient microtransactions, though only partially implemented. 
11.	Status Tracking: Displays remaining days until the project deadline, indicating whether funding is open or closed. User-Friendly UI/UX: Material-UI provides a clean interface, with progress bars and clear labeling for all functionalities.

Hardcoded Defaults: 
•	A fixed ETH-to-USD rate ($4000/ETH) is used to avoid external API calls and potential CORS issues during the demonstration.
•	Trusted signers for multi-sig and referral logic are predefined to ensure a stable and controlled demo environment.


How to Run the Project:	  Clone the Repository:  git clone https://github.com/The-Eminent/Adv-Blockchain-Final-Project cd decentralized-crowdfunding 
Install Dependencies: Ensure you have Node.js and Truffle installed.  npm install 
Set Up Ganache (or another local Ethereum network): Start Ganache (GUI or CLI). Ensure it runs at http://127.0.0.1:7545 by default or update the truffle-config.js accordingly.  Compile & Migrate Contracts:  truffle compile truffle migrate --reset 
Run the Frontend (React App):  cd client npm install npm start The app will open at http://localhost:3000.  Testing the Features:
	Name Registration: Connect MetaMask with your chosen account and set your name using the "Set My Name" button. 
	Create Project: Fill in the form (title, description, funding goal, deadline) and create a project. 
	Fund Project & Comments: Contribute a small amount of ETH via MetaMask and leave a comment. The top donor section and total funds update automatically. 
	Referral Links: Copy the referral link displayed under your account info and open it in another browser or account. Fund a project through that link to test referral counting. 
	Multi-Sig Approval: Attempt a withdrawal as a project creator once the goal is met. Switch to trusted signer accounts and approve the withdrawal. Once all required signers approve, the creator can successfully withdraw. 
	Micropayment Channel: Although partially implemented and tested off-chain with scripts, this conceptually shows how signed messages can transfer funds more efficiently.



