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

### 1.2 Bounties Covered

| **Bounty Name**  | **Sponsor**  | **Criteria Covered** |
|------------------|-------------|----------------------|
| Bounty # 1 | TODO | TODO |
| Bounty # 2 | TODO | TODO |
| Bounty # 3 | TODO | TODO |
| Bounty # 4 | TODO | TODO |

### 1.3 Team Members

| **Name** | **Role** | **GitHub / Twitter** |
|----------|---------|----------------------|
| Petar Popović | Smart Contract Dev | [X profile](https://x.com/0xdevelopera) |
| Milan Pajović | AI & Backend Engineer | [X profile](https://x.com/PajovicMilan) |
| Nikola Mitrović | Frontend & Backend Engineer | [X profile](https://x.com/mitrovicnik) |
| Aljoša Makević | Frontend Engineer | [X profile](https://x.com/aljoha_) |
| Petar Atanasovski | Product Manager | [X profile](https://x.com/atanasovskip) |

### 1.4 Demo Video & Important links

//TODO [![Demo Video](https://img.youtube.com/vi/YOUR_VIDEO_ID/0.jpg)](https://youtu.be/YOUR_VIDEO_ID)

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
| TODO | TODO | [GitHub Link](https://github.com/) |
| TODO | TODO | [GitHub Link](https://github.com/) |
| TODO | TODO | [GitHub Link](https://github.com/) |

### 2.4 API Endpoints

### 2.5 Bounties Description

### 2.6. How to Run the Project

#### 2.6.1. Prerequisites

#### 2.6.2. Installation

#### 2.6.3. Deploy Smart Contracts

#### 2.6.4. Run Backend & AI Agents

## 3. Product Documentation

### 3.1 MVP Scope

### 3.2 Long-Term Product Vision

### 3.3 Clickable Prototypes

