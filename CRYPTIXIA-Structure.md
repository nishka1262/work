# CRYPTIXIA - Complete Repository Structure Documentation

## Table of Contents

1. [Project Overview](#project-overview)
2. [Root Directory Structure](#root-directory-structure)
3. [Frontend Structure (Next.js + TypeScript)](#frontend-structure)
4. [Server Structure (Node.js + Express)](#server-structure)
5. [Blockchain Structure (Solidity + Foundry)](#blockchain-structure)
6. [AI Models Structure](#ai-models-structure)
7. [Documentation Structure](#documentation-structure)
8. [Docker & DevOps](#docker--devops)
9. [Development Commands](#development-commands)

---

## Project Overview

CRYPTIXIA is a comprehensive platform for AI agent creation, training, and trading with blockchain integration. The project consists of multiple interconnected components including a Next.js frontend, Node.js backend, Solidity smart contracts, and AI training modules.

---

## Root Directory Structure

```
cryptixia/
├── frontend/                    # Next.js React Frontend
├── server/                      # Node.js Backend API
├── blockchain/                  # Solidity Smart Contracts
├── ai-models/                   # AI Training & Model Files
├── docs/                        # Documentation
├── scripts/                     # Deployment & Utility Scripts
├── docker/                      # Docker Configuration
├── .github/                     # GitHub Actions CI/CD
├── README.md
├── package.json                 # Root package.json for monorepo
└── docker-compose.yml           # Full stack docker setup
```

---

## Frontend Structure

**Technology Stack:** Next.js + TypeScript + React

### Component Architecture

```
frontend/
├── components/
│   ├── agent/                   # Agent-related components
│   │   ├── AgentCard.tsx        # Display agent info
│   │   ├── AgentProfile.tsx     # Detailed agent view
│   │   ├── AgentMarketplace.tsx # Trading interface
│   │   └── AgentEvolution.tsx   # Evolution/breeding UI
│   │
│   ├── chat/                    # Chat interface components
│   │   ├── ChatUI.tsx           # Main chat interface
│   │   ├── ChatHistory.tsx      # Conversation history
│   │   ├── VoiceButton.tsx      # Voice input
│   │   ├── VoiceTransfer.tsx    # Voice processing
│   │   └── MessageBubble.tsx    # Individual messages
│   │
│   ├── training/                # Training interface components
│   │   ├── TrainingDashboard.tsx     # Main training interface
│   │   ├── MemoryViewer.tsx          # View agent memories
│   │   ├── SkillBuilder.tsx          # Teach skills
│   │   ├── HabitTracker.tsx          # Track user habits
│   │   ├── VoiceTrainer.tsx          # Voice training
│   │   ├── ConversationLogger.tsx    # Training conversations
│   │   └── TrainingProgress.tsx      # Progress visualization
│   │
│   ├── breeding/                # Breeding system components
│   │   ├── BreedingInterface.tsx     # Agent breeding
│   │   ├── GeneticViewer.tsx         # Show agent genetics
│   │   ├── CompatibilityChecker.tsx  # Check breeding compatibility
│   │   └── OffspringPreview.tsx      # Preview new agent
│   │
│   ├── wallet/                  # Wallet integration components
│   │   ├── WalletConnector.tsx       # Wallet connection
│   │   ├── WalletTest.tsx            # Testing interface
│   │   ├── Web3Provider.tsx          # Web3 context
│   │   └── TransactionStatus.tsx     # TX status tracking
│   │
│   ├── mint/                    # Agent minting components
│   │   ├── MintForm.tsx              # Agent minting form
│   │   ├── MintFormClient.tsx        # Client-side mint logic
│   │   ├── PersonalitySelector.tsx   # Choose personality traits
│   │   └── MintPreview.tsx           # Preview before minting
│   │
│   ├── marketplace/             # Marketplace components
│   │   ├── MarketplaceGrid.tsx       # Agent listings
│   │   ├── AgentListing.tsx          # Individual listings
│   │   ├── BuyModal.tsx              # Purchase modal
│   │   ├── SellModal.tsx             # Sell modal
│   │   └── RentModal.tsx             # Rental system
│   │
│   └── ui/                      # Reusable UI components
│       ├── Button.tsx                # Reusable button
│       ├── Modal.tsx                 # Modal component
│       ├── LoadingSpinner.tsx        # Loading states
│       ├── Toast.tsx                 # Notifications
│       └── Layout.tsx                # Page layout
```

### Pages Structure

```
pages/
├── api/                          # Next.js API routes (proxy)
│   └── proxy/
│       ├── chat.ts               # Chat API proxy
│       ├── training.ts           # Training API proxy
│       └── agents.ts             # Agent API proxy
│
├── agent/                        # Agent-related pages
│   ├── [id].tsx                  # Agent detail page
│   ├── mint.tsx                  # Minting page
│   └── marketplace.tsx           # Marketplace page
│
├── training/                     # Training pages
│   ├── index.tsx                 # Training dashboard
│   ├── conversation.tsx          # Chat training
│   ├── voice.tsx                 # Voice training
│   ├── skills.tsx                # Skill training
│   └── memories.tsx              # Memory management
│
├── breeding/                     # Breeding pages
│   ├── index.tsx                 # Breeding interface
│   └── genetics.tsx              # Genetic viewer
│
├── wallet/
│   └── test.tsx                  # Wallet testing
│
├── _app.tsx                      # App wrapper
├── _document.tsx                 # HTML document
├── index.tsx                     # Landing page
└── demo.tsx                      # Demo page
```

### Supporting Files

```
├── hooks/                        # Custom React hooks
│   ├── useAgent.ts               # Agent management
│   ├── useChat.ts                # Chat functionality
│   ├── useTraining.ts            # Training operations
│   ├── useWallet.ts              # Wallet operations
│   ├── useMemory.ts              # Memory management
│   └── useBreeding.ts            # Breeding operations
│
├── lib/                          # Utility libraries
│   ├── web3.ts                   # Web3 utilities
│   ├── api.ts                    # API client
│   ├── storage.ts                # Local storage utils
│   ├── encryption.ts             # Client-side encryption
│   └── constants.ts              # App constants
│
├── types/                        # TypeScript definitions
│   ├── agent.ts                  # Agent type definitions
│   ├── memory.ts                 # Memory types
│   ├── training.ts               # Training types
│   ├── breeding.ts               # Breeding types
│   └── api.ts                    # API response types
```

---

## Server Structure

**Technology Stack:** Node.js + Express + MongoDB

### Controllers Layer

```
src/controllers/
├── agentController.js        # Agent CRUD operations
├── trainingController.js     # Training sessions
├── memoryController.js       # Memory management
├── conversationController.js # Chat handling
├── voiceController.js        # Voice processing
├── breedingController.js     # Agent breeding
├── marketplaceController.js  # Marketplace operations
├── userController.js         # User management
├── blockchainController.js   # Web3 interactions
└── analyticsController.js    # Analytics & insights
```

### Data Models

```
src/models/
├── Agent.js                  # Agent schema
├── Memory.js                 # Memory records
├── Conversation.js           # Chat history
├── Training.js               # Training sessions
├── User.js                   # User profiles
├── Skill.js                  # Learned skills
├── Breeding.js               # Breeding records
├── Transaction.js            # Blockchain transactions
└── Marketplace.js            # Marketplace listings
```

### Services Layer

#### AI Services
```
src/services/ai/
├── aiService.js          # Main AI service
├── openaiService.js      # OpenAI integration
├── claudeService.js      # Anthropic Claude
├── localAIService.js     # Local AI models
└── promptService.js      # Prompt management
```

#### Memory Services
```
src/services/memory/
├── memoryService.js      # Core memory operations
├── vectorDBService.js    # Vector database
├── embeddingService.js   # Text embeddings
└── consolidationService.js # Memory consolidation
```

#### Voice Services
```
src/services/voice/
├── voiceService.js       # Voice processing
├── speechToTextService.js # STT conversion
├── textToSpeechService.js # TTS conversion
└── voiceCloningService.js # Voice cloning
```

#### Blockchain Services
```
src/services/blockchain/
├── blockchainService.js  # Main blockchain service
├── web3Service.js        # Web3 operations
├── nftService.js         # NFT operations
├── contractService.js    # Smart contract calls
└── eventListenerService.js # Blockchain events
```

#### Storage Services
```
src/services/storage/
├── ipfsService.js        # IPFS operations
├── fileUploadService.js  # File handling
├── encryptionService.js  # Data encryption
└── backupService.js      # Data backup
```

#### Personality & Training Services
```
src/services/personality/
├── personalityService.js # Personality modeling
├── traitService.js       # Trait management
├── evolutionService.js   # Personality evolution
└── breedingService.js    # Trait breeding

src/services/training/
├── trainingService.js    # Core training logic
├── skillExtractionService.js # Extract skills
├── habitLearningService.js # Learn habits
└── progressTrackingService.js # Track progress
```

### Middleware & Routes

```
src/middleware/
├── auth.js                   # Wallet authentication
├── rateLimiter.js           # API rate limiting
├── validation.js            # Input validation
├── encryption.js            # Request encryption
├── cors.js                  # CORS configuration
├── errorHandler.js          # Error handling
└── logging.js               # Request logging

src/routes/
├── agents.js                # /api/agents/*
├── training.js              # /api/training/*
├── memory.js                # /api/memory/*
├── conversation.js          # /api/chat/*
├── voice.js                 # /api/voice/*
├── breeding.js              # /api/breeding/*
├── marketplace.js           # /api/marketplace/*
├── users.js                 # /api/users/*
├── blockchain.js            # /api/blockchain/*
└── analytics.js             # /api/analytics/*
```

### Utilities & Background Jobs

```
src/utils/
├── database/                # Database utilities
├── crypto/                  # Cryptographic functions
├── ai/                      # AI-specific utilities
└── general/                 # General utilities

src/jobs/
├── memoryConsolidation.js   # Background memory processing
├── modelTraining.js         # AI model training jobs
├── blockchainSync.js        # Sync blockchain data
├── backupData.js            # Data backup jobs
└── cleanup.js               # Cleanup old data
```

---

## Blockchain Structure

**Technology Stack:** Solidity + Foundry + OpenZeppelin

### Core Contracts

```
src/core/
├── CryptixiaAgent.sol       # Main Agent NFT contract
├── AgentFactory.sol         # Agent creation factory
├── AgentRegistry.sol        # Agent registry & metadata
└── AgentUpgradeable.sol     # Upgradeable agent logic
```

### Specialized Contract Modules

#### Memory Management
```
src/memory/
├── MemoryStorage.sol        # On-chain memory storage
├── MemoryVerification.sol   # Verify memory integrity
└── MemoryAccess.sol         # Memory access control
```

#### Breeding System
```
src/breeding/
├── AgentBreeding.sol        # Breeding mechanics
├── GeneticAlgorithm.sol     # Genetic trait mixing
├── TraitInheritance.sol     # Trait inheritance rules
└── BreedingMarketplace.sol  # Breeding marketplace
```

#### Marketplace Contracts
```
src/marketplace/
├── AgentMarketplace.sol     # Buy/sell agents
├── RentalSystem.sol         # Agent rental system
├── Escrow.sol               # Transaction escrow
└── AuctionHouse.sol         # Agent auctions
```

#### Training & Rewards
```
src/training/
├── TrainingRewards.sol      # Training incentives
├── SkillCertification.sol   # Skill verification
└── ProgressTracking.sol     # Training progress
```

#### Governance & Tokens
```
src/governance/
├── CryptixiaDAO.sol         # DAO governance
├── ProposalSystem.sol       # Community proposals
└── VotingMechanism.sol      # Voting system

src/tokens/
├── CryptixiaToken.sol       # Platform utility token
├── RewardDistribution.sol   # Reward distribution
└── Staking.sol              # Token staking
```

### Testing & Deployment

```
test/
├── unit/                    # Unit tests for individual contracts
├── integration/             # Integration tests
└── mocks/                   # Mock contracts for testing

script/
├── deployment/              # Deployment scripts
├── setup/                   # Contract initialization
└── maintenance/             # Maintenance scripts

deployments/
├── mainnet/                 # Mainnet deployment info
├── sepolia/                 # Testnet deployment info
└── localhost/               # Local deployment info
```

---

## AI Models Structure

### Training Infrastructure

```
ai-models/
├── training/
│   ├── datasets/
│   │   ├── conversations/           # Training conversations
│   │   ├── personalities/           # Personality datasets
│   │   ├── skills/                  # Skill training data
│   │   └── voices/                  # Voice training samples
│   │
│   ├── scripts/
│   │   ├── train_personality.py     # Personality model training
│   │   ├── train_memory.py          # Memory model training
│   │   ├── train_voice.py           # Voice cloning training
│   │   └── fine_tune.py             # Model fine-tuning
│   │
│   └── configs/
│       ├── personality_config.yaml  # Personality model config
│       ├── memory_config.yaml       # Memory model config
│       └── voice_config.yaml        # Voice model config
```

### Model Storage & Inference

```
├── models/
│   ├── personality/                 # Personality models
│   ├── memory/                      # Memory consolidation models
│   ├── voice/                       # Voice synthesis models
│   └── embeddings/                  # Text embedding models
│
├── inference/
│   ├── personality_inference.py     # Personality generation
│   ├── memory_retrieval.py          # Memory retrieval
│   ├── voice_synthesis.py           # Voice generation
│   └── context_building.py          # Context building
```

### Evaluation & Utilities

```
├── evaluation/
│   ├── personality_eval.py          # Evaluate personality models
│   ├── memory_eval.py               # Evaluate memory systems
│   └── voice_eval.py                # Evaluate voice quality
│
├── utils/
│   ├── data_preprocessing.py        # Data preprocessing
│   ├── model_utils.py               # Model utilities
│   └── evaluation_metrics.py       # Evaluation metrics
```

---

## Documentation Structure

### Technical Documentation

```
docs/
├── architecture/
│   ├── system-overview.md           # System architecture
│   ├── frontend-architecture.md    # Frontend structure
│   ├── backend-architecture.md     # Backend structure
│   ├── blockchain-architecture.md  # Smart contract structure
│   └── ai-architecture.md          # AI system structure
│
├── api/
│   ├── api-reference.md             # Complete API reference
│   ├── authentication.md           # Auth documentation
│   ├── rate-limiting.md             # Rate limiting info
│   └── webhooks.md                  # Webhook documentation
│
├── smart-contracts/
│   ├── contract-overview.md         # Contract overview
│   ├── deployment-guide.md         # Deployment instructions
│   ├── interaction-guide.md        # How to interact
│   └── security-audit.md           # Security considerations
```

### User & Developer Guides

```
├── ai-training/
│   ├── training-overview.md         # AI training process
│   ├── personality-training.md     # Personality model training
│   ├── memory-system.md             # Memory system docs
│   └── voice-cloning.md             # Voice cloning process
│
├── user-guides/
│   ├── getting-started.md           # Quick start guide
│   ├── creating-agents.md           # Agent creation guide
│   ├── training-agents.md           # Training guide
│   ├── breeding-agents.md           # Breeding guide
│   └── marketplace-guide.md         # Marketplace usage
│
├── developer-guides/
│   ├── setup-development.md         # Development setup
│   ├── contributing.md              # Contribution guidelines
│   ├── coding-standards.md         # Code style guide
│   └── testing-guide.md             # Testing procedures
```

### Deployment Documentation

```
└── deployment/
    ├── production-deployment.md     # Production setup
    ├── docker-deployment.md        # Docker deployment
    ├── aws-deployment.md           # AWS deployment
    └── monitoring-setup.md         # Monitoring & logging
```

---

## Docker & DevOps

### Development Environment

```
docker/
├── development/
│   ├── docker-compose.dev.yml       # Development environment
│   ├── Dockerfile.frontend          # Frontend dev container
│   ├── Dockerfile.backend           # Backend dev container
│   └── Dockerfile.blockchain        # Blockchain dev container
```

### Production Environment

```
├── production/
│   ├── docker-compose.prod.yml      # Production environment
│   ├── Dockerfile.frontend.prod     # Production frontend
│   ├── Dockerfile.backend.prod      # Production backend
│   └── nginx.conf                   # Nginx configuration
```

### Monitoring & CI/CD

```
├── monitoring/
│   ├── prometheus.yml               # Prometheus config
│   ├── grafana-dashboard.json       # Grafana dashboard
│   └── alertmanager.yml             # Alert configuration
│
└── .github/workflows/
    ├── frontend-ci.yml              # Frontend CI/CD
    ├── backend-ci.yml               # Backend CI/CD
    ├── blockchain-ci.yml            # Smart contract CI/CD
    └── security-audit.yml           # Security checks
```

---

## Development Commands

### Root Level Commands
```bash
npm install                          # Install all dependencies
npm run dev                          # Start all services
npm run build                        # Build all projects
npm run test                         # Run all tests
npm run deploy                       # Deploy to staging
```

### Individual Service Commands
```bash
npm run frontend:dev                 # Start frontend only
npm run backend:dev                  # Start backend only
npm run blockchain:test              # Test smart contracts
npm run ai:train                     # Train AI models
```

### Deployment Scripts
```bash
./scripts/setup-dev.sh               # Development setup
./scripts/deploy-staging.sh          # Staging deployment
./scripts/deploy-production.sh       # Production deployment
./scripts/backup-data.sh             # Data backup
```

---

## Key Features

### Agent Management
- **Creation**: Mint new AI agents with customizable personalities
- **Training**: Interactive training through conversations and skill building
- **Memory**: Persistent memory system with consolidation
- **Evolution**: Agent personality development over time

### Blockchain Integration
- **NFT Agents**: Each agent is a unique NFT on the blockchain
- **Breeding**: Genetic algorithm-based agent breeding
- **Marketplace**: Buy, sell, and rent AI agents
- **Governance**: DAO-based platform governance

### AI Capabilities
- **Personality Models**: Custom AI models for personality traits
- **Voice Cloning**: Personalized voice synthesis
- **Memory System**: Advanced memory consolidation and retrieval
- **Skill Learning**: Dynamic skill acquisition through training

### Technical Infrastructure
- **Scalable Architecture**: Microservices-based design
- **Real-time Communication**: WebSocket-based chat system
- **Secure Storage**: Encrypted data storage with IPFS integration
- **Monitoring**: Comprehensive logging and analytics

---

*This document serves as a complete reference for the CRYPTIXIA project structure and can be used for development, deployment, and maintenance purposes.*
