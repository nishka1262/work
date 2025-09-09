# CRYPTIXIA - Complete Repository Structure

## 🏗 Root Directory Structure
cryptixia/
├── frontend/ # Next.js React Frontend
├── server/ # Node.js Backend API
├── blockchain/ # Solidity Smart Contracts
├── ai-models/ # AI Training & Model Files
├── docs/ # Documentation
├── scripts/ # Deployment & Utility Scripts
├── docker/ # Docker Configuration
├── .github/ # GitHub Actions CI/CD
├── README.md
├── package.json # Root package.json for monorepo
└── docker-compose.yml # Full stack docker setup

shell
Copy code

## 🎨 Frontend Structure (Next.js + TypeScript)
frontend/
├── components/
│ ├── agent/
│ │ ├── AgentCard.tsx
│ │ ├── AgentProfile.tsx
│ │ ├── AgentMarketplace.tsx
│ │ └── AgentEvolution.tsx
│ ├── chat/
│ │ ├── ChatUI.tsx
│ │ ├── ChatHistory.tsx
│ │ ├── VoiceButton.tsx
│ │ ├── VoiceTransfer.tsx
│ │ └── MessageBubble.tsx
│ ├── training/
│ │ ├── TrainingDashboard.tsx
│ │ ├── MemoryViewer.tsx
│ │ ├── SkillBuilder.tsx
│ │ ├── HabitTracker.tsx
│ │ ├── VoiceTrainer.tsx
│ │ ├── ConversationLogger.tsx
│ │ └── TrainingProgress.tsx
│ ├── breeding/
│ │ ├── BreedingInterface.tsx
│ │ ├── GeneticViewer.tsx
│ │ ├── CompatibilityChecker.tsx
│ │ └── OffspringPreview.tsx
│ ├── wallet/
│ │ ├── WalletConnector.tsx
│ │ ├── WalletTest.tsx
│ │ ├── Web3Provider.tsx
│ │ └── TransactionStatus.tsx
│ ├── mint/
│ │ ├── MintForm.tsx
│ │ ├── MintFormClient.tsx
│ │ ├── PersonalitySelector.tsx
│ │ └── MintPreview.tsx
│ ├── marketplace/
│ │ ├── MarketplaceGrid.tsx
│ │ ├── AgentListing.tsx
│ │ ├── BuyModal.tsx
│ │ ├── SellModal.tsx
│ │ └── RentModal.tsx
│ └── ui/
│ ├── Button.tsx
│ ├── Modal.tsx
│ ├── LoadingSpinner.tsx
│ ├── Toast.tsx
│ └── Layout.tsx
├── pages/
│ ├── api/
│ │ └── proxy/
│ │ ├── chat.ts
│ │ ├── training.ts
│ │ └── agents.ts
│ ├── agent/
│ │ ├── [id].tsx
│ │ ├── mint.tsx
│ │ └── marketplace.tsx
│ ├── training/
│ │ ├── index.tsx
│ │ ├── conversation.tsx
│ │ ├── voice.tsx
│ │ ├── skills.tsx
│ │ └── memories.tsx
│ ├── breeding/
│ │ ├── index.tsx
│ │ └── genetics.tsx
│ ├── wallet/
│ │ └── test.tsx
│ ├── _app.tsx
│ ├── _document.tsx
│ ├── index.tsx
│ └── demo.tsx
├── hooks/
│ ├── useAgent.ts
│ ├── useChat.ts
│ ├── useTraining.ts
│ ├── useWallet.ts
│ ├── useMemory.ts
│ └── useBreeding.ts
├── lib/
│ ├── web3.ts
│ ├── api.ts
│ ├── storage.ts
│ ├── encryption.ts
│ └── constants.ts
├── styles/
│ ├── globals.css
│ ├── components.css
│ └── tailwind.css
├── types/
│ ├── agent.ts
│ ├── memory.ts
│ ├── training.ts
│ ├── breeding.ts
│ └── api.ts
├── public/
│ ├── images/
│ ├── icons/
│ └── sounds/
├── next.config.js
├── tailwind.config.js
├── tsconfig.json
└── package.json

shell
Copy code

## 🖥 Server Structure (Node.js + Express)
server/
├── src/
│ ├── controllers/
│ ├── models/
│ ├── services/
│ ├── middleware/
│ ├── routes/
│ ├── utils/
│ ├── jobs/
│ ├── config/
│ └── app.js
├── tests/
├── scripts/
├── logs/
├── uploads/
├── .env.example
├── .gitignore
├── Dockerfile
├── docker-compose.yml
├── package.json
└── README.md

shell
Copy code

## ⛓ Blockchain Structure (Solidity + Foundry)
blockchain/
├── src/
│ ├── core/
│ ├── memory/
│ ├── breeding/
│ ├── marketplace/
│ ├── training/
│ ├── governance/
│ ├── tokens/
│ ├── utils/
│ └── interfaces/
├── test/
├── script/
├── lib/
├── deployments/
├── abi/
├── docs/
├── foundry.toml
├── remappings.txt
├── .env.example
├── .gitignore
└── README.md

shell
Copy code

## 🤖 AI Models Structure
ai-models/
├── training/
├── models/
├── inference/
├── evaluation/
├── utils/
└── requirements.txt

shell
Copy code

## 📚 Documentation Structure
docs/
├── architecture/
├── api/
├── smart-contracts/
├── ai-training/
├── user-guides/
├── developer-guides/
└── deployment/

shell
Copy code

## 🐳 Docker & DevOps
docker/
├── development/
├── production/
└── monitoring/

shell
Copy code

## 🚀 Root Configuration Files
cryptixia/
├── .github/
├── scripts/
├── package.json
├── docker-compose.yml
├── .gitignore
├── .env.example
├── README.md
├── LICENSE
└── CONTRIBUTING.md

shell
Copy code

## 🔧 Development Commands
Root level
npm install
npm run dev
npm run build
npm run test
npm run deploy

Individual services
npm run frontend:dev
npm run backend:dev
npm run blockchain:test
npm run ai:train

Copy code
