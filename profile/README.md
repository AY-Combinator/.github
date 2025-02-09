# AY Combinator Project Documentation
ETH Global Agentic Ethereum Hackathon 

Licence - This project is licensed under the MIT License.

## 1. Introduction

### 1.1 Brief Project Description
AY Combinator is an **AI-powered Web3 startup incubator operating as a DAO**, leveraging autonomous AI agents to guide founders through the program, evaluate projects, and allocate funding through **on-chain governance and investment smart contracts**.

**Target Users**

- Web3 Startup Founders – Seeking structured incubation, mentorship, and quick access to capital.
- Investors – Looking for high-quality, AI-vetted Web3 startups aligned with their investment thesis.
- Mentors & Ecosystem Builders – Engaging in AI-assisted startup evaluations.

**Problem & Solution**

**Problem:** Traditional incubators are very costly, have limited throughput and high risk for investors. Founders lack efficient way to cover all loose ends, find product market fit and get access to capital.

**Solution:** AY Combinator automates startup evaluation, mentorship, and investment decisions. AI Agents guide founders through structured modules, provide feedback, score progress, and allocate on-chain funding when milestones and criteria set by the DAO members are met.

**AI Agent Roles**

- Agent Coach – Guides founders with structured questions and ensures completion of key modules.
- Agent Mentor – Provides market insights, feedback, and auto-completes assumptions.
- Agent Judge – Scores startups based on structured criteria, providing objective evaluation.
- Agent Investor – Analyzes startups with on-chain governance rules and deploys USDC investments from DAO funds.

### 1.2 Team Members

| **Name** | **Role** | **GitHub / Twitter** |
|----------|---------|----------------------|
| Petar Popović | Smart Contract Dev | [X profile](https://x.com/0xdevelopera) |
| Milan Pajović | AI & Backend Engineer | [X profile](https://x.com/PajovicMilan) |
| Nikola Mitrović | Frontend & Backend Engineer | [X profile](https://x.com/mitrovicnik) |
| Aljoša Makević | Frontend Engineer | [X profile](https://x.com/aljoha_) |
| Petar Atanasovski | Product Manager | [X profile](https://x.com/atanasovskip) |

### 1.3 Demo Video & Important links

[![Demo Video](https://drive.google.com/file/d/1WAcOW3FYmUJtDhkQ7AV2oWaY56SFfdpq/view?usp=sharing)

---

## 2. Tech Architecture

### 2.1 Overall Architecture Diagram


### 2.2 Sequence Diagrams

#### Overall Project
![image](https://github.com/user-attachments/assets/11df88e7-6358-45f4-b9ad-7fdf5cd4a9cd)

```
sequenceDiagram
    participant LP as LP Investors
    participant DTY as DAO Treasury
    participant DT as DAO Team
    participant SF as Startup Founder
    participant AC as Agent Coach
    participant AM as Agent Mentor
    participant AJ as Agent Judge
    participant AI as Agent Investor

    %% Step 1: LP Investors deposit funds into DAO
    LP->>DTY: Deposit USDC
    DTY->>LP: Issue governance tokens

    %% Step 2: DAO deducts fees and allocates ownership
    DTY->>DT: Deduct 5% management fee
    DTY-->>LP: Remaining 95% distributed as governance tokens

    %% Step 3: Startup Founder creates a project
    SF->>AC: Create new project

    loop Module Iteration (Problem Framing, User Persona, etc.)
        AC->>SF: Guides through module
        SF->>AC: Provides answers
        AC->>AM: Requests feedback & market data
        AM->>AC: Provides insights
        AC->>AJ: Requests scoring & critique
        AJ->>SF: Sends score & feedback
    end

    %% Step 4: Scoring & Investment Eligibility Check
    AJ->>DTY: Check if score >= 900/1000
    DTY-->>AJ: Confirm eligibility

    %% Step 5: Founder submits investment terms
    SF->>AI: Submit investment terms
    note right of SF: Investment Terms:<br/>- Valuation<br/>- Deal Size<br/>- Token Lockup Period<br/>- % Equity/Tokens Offered

    AI->>DTY: Evaluate investment
    DTY-->>AI: Approve investment
    AI->>SF: Deploy USDC

    %% Step 6: Profits Realization & Distribution
    SF->>DTY: Returns on investment (profit realized)
    DTY->>DT: Allocate 10% Carried Interest
    DTY->>LP: Distribute 90% profits to LPs based on governance tokens
```

### 2.3 Repositories

| **Repo** | **Description** | **Link** |
|----------|---------------|---------|
| .github | TODO | [GitHub Link](https://github.com/AY-Combinator/.github) |
| webapp | TODO | [GitHub Link](https://github.com/AY-Combinator/webapp) |
| ai_agent | TODO | [GitHub Link](https://github.com/AY-Combinator/ai_agent) |
| contracts | TODO | [GitHub Link](https://github.com/AY-Combinator/contracts) |

### 2.4 API Endpoints

### 2.5 Bounties Description



### 2.6. How to Run the Project

#### 2.6.1. Prerequisites

#### 2.6.2. Installation

#### 2.6.3. Deploy Smart Contracts

To manage investments and governance, AY Combinator has deployed smart contracts on the Base blockchain network:

StartupDepositContract: Manages deposits from startups. Address: https://base-sepolia.blockscout.com/address/0xee7Ffb3A5b48c391aC171304d37DEeD9Bb3dB730
InvestorDepositContract: Handles investor funds and issues corresponding governance tokens. Address: https://base-sepolia.blockscout.com/address/0x16Fb8E786347B6Ab1f6114BacbAfb6Ed7970C754
GovernanceTokenContract: Manages the distribution and governance of tokens within the DAO. Address: https://base-sepolia.blockscout.com/address/0xe9d81f422215480eD02294867796163B88994C33
MockUSDC: Mocked tokens for testing purposes. Address: https://base-sepolia.blockscout.com/address/0xA7c9B5c961B9D7bfa3588Bc3b29a609806093A3f 

Testing steps:
1. Deploy MockUSDC Contract, AYC Governance Token Contract
2. Deploy Startup Deposit and Investor Deposit Contracts
3. Mint yourself MockUSDC
4. Send MockUSDC to Investor Deposit Contract & Receive in turn AYC Governance Token Contracts 
5. Once startup founders realizes planned profits, receive amount of funds corresponding to amount of AYC Governance tokens

With the initial deployment of MockUSDC Contract and Investor Deposit Contract, we are able to send mocked USDC funds to the Investor Deposit Contract. In turn we become LP Investors that receive Mocked AYC Governance Tokens (LP Tokens) from the AYC Governance Token Contract. Startups later send realized profits to the StartupDepositContract, which allocates funds accordingly—10% as carried interest and 90% to investor LPs based on governance tokens.


#### 2.6.4. Run Backend & AI Agents

## 3. Product Documentation

### 3.1 MVP Scope

### 3.2 Long-Term Product Vision

### 3.3 Clickable Prototypes

