# CRYPTIXIA
## Complete Repository Structure Documentation



## Table of Contents

1. [Root Directory Structure](#1-root-directory-structure)
2. [Frontend Structure](#2-frontend-structure)  
3. [Server Structure](#3-server-structure)
4. [Blockchain Structure](#4-blockchain-structure)
5. [AI Models Structure](#5-ai-models-structure)
6. [Documentation Structure](#6-documentation-structure)
7. [Docker & DevOps](#7-docker--devops)
8. [Root Configuration Files](#8-root-configuration-files)
9. [Development Commands](#9-development-commands)

---

## 1. Root Directory Structure

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

## 2. Frontend Structure
**Technology Stack:** Next.js + TypeScript

### Component Architecture

```
frontend/
├── components/
│   ├── agent/
│   │   ├── AgentCard.tsx             # Display agent info
│   │   ├── AgentProfile.tsx          # Detailed agent view
│   │   ├── AgentMarketplace.tsx      # Trading interface
│   │   └── AgentEvolution.tsx        # Evolution/breeding UI
│   │
│   ├── chat/
│   │   ├── ChatUI.tsx                # Main chat interface
│   │   ├── ChatHistory.tsx           # Conversation history
│   │   ├── VoiceButton.tsx           # Voice input
│   │   ├── VoiceTransfer.tsx         # Voice processing
│   │   └── MessageBubble.tsx         # Individual messages
│   │
│   ├── training/
│   │   ├── TrainingDashboard.tsx     # Main training interface
│   │   ├── MemoryViewer.tsx          # View agent memories
│   │   ├── SkillBuilder.tsx          # Teach skills
│   │   ├── HabitTracker.tsx          # Track user habits
│   │   ├── VoiceTrainer.tsx          # Voice training
│   │   ├── ConversationLogger.tsx    # Training conversations
│   │   └── TrainingProgress.tsx      # Progress visualization
│   │
│   ├── breeding/
│   │   ├── BreedingInterface.tsx     # Agent breeding
│   │   ├── GeneticViewer.tsx         # Show agent genetics
│   │   ├── CompatibilityChecker.tsx  # Check breeding compatibility
│   │   └── OffspringPreview.tsx      # Preview new agent
│   │
│   ├── wallet/
│   │   ├── WalletConnector.tsx       # Wallet connection
│   │   ├── WalletTest.tsx            # Testing interface
│   │   ├── Web3Provider.tsx          # Web3 context
│   │   └── TransactionStatus.tsx     # TX status tracking
│   │
│   ├── mint/
│   │   ├── MintForm.tsx              # Agent minting form
│   │   ├── MintFormClient.tsx        # Client-side mint logic
│   │   ├── PersonalitySelector.tsx   # Choose personality traits
│   │   └── MintPreview.tsx           # Preview before minting
│   │
│   ├── marketplace/
│   │   ├── MarketplaceGrid.tsx       # Agent listings
│   │   ├── AgentListing.tsx          # Individual listings
│   │   ├── BuyModal.tsx              # Purchase modal
│   │   ├── SellModal.tsx             # Sell modal
│   │   └── RentModal.tsx             # Rental system
│   │
│   └── ui/
│       ├── Button.tsx                # Reusable button
│       ├── Modal.tsx                 # Modal component
│       ├── LoadingSpinner.tsx        # Loading states
│       ├── Toast.tsx                 # Notifications
│       └── Layout.tsx                # Page layout
```

### Pages Structure

```
├── pages/
│   ├── api/                          # Next.js API routes (proxy)
│   │   ├── proxy/
│   │   │   ├── chat.ts               # Chat API proxy
│   │   │   ├── training.ts           # Training API proxy
│   │   │   └── agents.ts             # Agent API proxy
│   │
│   ├── agent/
│   │   ├── [id].tsx                  # Agent detail page
│   │   ├── mint.tsx                  # Minting page
│   │   └── marketplace.tsx           # Marketplace page
│   │
│   ├── training/
│   │   ├── index.tsx                 # Training dashboard
│   │   ├── conversation.tsx          # Chat training
│   │   ├── voice.tsx                 # Voice training
│   │   ├── skills.tsx                # Skill training
│   │   └── memories.tsx              # Memory management
│   │
│   ├── breeding/
│   │   ├── index.tsx                 # Breeding interface
│   │   └── genetics.tsx              # Genetic viewer
│   │
│   ├── wallet/
│   │   └── test.tsx                  # Wallet testing
│   │
│   ├── _app.tsx                      # App wrapper
│   ├── _document.tsx                 # HTML document
│   ├── index.tsx                     # Landing page
│   └── demo.tsx                      # Demo page
```

### Supporting Libraries

```
├── hooks/
│   ├── useAgent.ts                   # Agent management
│   ├── useChat.ts                    # Chat functionality
│   ├── useTraining.ts                # Training operations
│   ├── useWallet.ts                  # Wallet operations
│   ├── useMemory.ts                  # Memory management
│   └── useBreeding.ts                # Breeding operations
│
├── lib/
│   ├── web3.ts                       # Web3 utilities
│   ├── api.ts                        # API client
│   ├── storage.ts                    # Local storage utils
│   ├── encryption.ts                 # Client-side encryption
│   └── constants.ts                  # App constants
│
├── styles/
│   ├── globals.css                   # Global styles
│   ├── components.css                # Component styles
│   └── tailwind.css                  # Tailwind imports
│
├── types/
│   ├── agent.ts                      # Agent type definitions
│   ├── memory.ts                     # Memory types
│   ├── training.ts                   # Training types
│   ├── breeding.ts                   # Breeding types
│   └── api.ts                        # API response types
│
├── public/
│   ├── images/
│   ├── icons/
│   └── sounds/
│
├── next.config.js
├── tailwind.config.js
├── tsconfig.json
└── package.json
```

---

## 3. Server Structure
**Technology Stack:** Node.js + Express

### Core Application Structure

```
server/
├── src/
│   ├── controllers/
│   │   ├── agentController.js        # Agent CRUD operations
│   │   ├── trainingController.js     # Training sessions
│   │   ├── memoryController.js       # Memory management
│   │   ├── conversationController.js # Chat handling
│   │   ├── voiceController.js        # Voice processing
│   │   ├── breedingController.js     # Agent breeding
│   │   ├── marketplaceController.js  # Marketplace operations
│   │   ├── userController.js         # User management
│   │   ├── blockchainController.js   # Web3 interactions
│   │   └── analyticsController.js    # Analytics & insights
│   │
│   ├── models/
│   │   ├── Agent.js                  # Agent schema
│   │   ├── Memory.js                 # Memory records
│   │   ├── Conversation.js           # Chat history
│   │   ├── Training.js               # Training sessions
│   │   ├── User.js                   # User profiles
│   │   ├── Skill.js                  # Learned skills
│   │   ├── Breeding.js               # Breeding records
│   │   ├── Transaction.js            # Blockchain transactions
│   │   └── Marketplace.js            # Marketplace listings
```

### Service Layer Architecture

```
│   ├── services/
│   │   ├── ai/
│   │   │   ├── aiService.js          # Main AI service
│   │   │   ├── openaiService.js      # OpenAI integration
│   │   │   ├── claudeService.js      # Anthropic Claude
│   │   │   ├── localAIService.js     # Local AI models
│   │   │   └── promptService.js      # Prompt management
│   │   │
│   │   ├── memory/
│   │   │   ├── memoryService.js      # Core memory operations
│   │   │   ├── vectorDBService.js    # Vector database
│   │   │   ├── embeddingService.js   # Text embeddings
│   │   │   └── consolidationService.js # Memory consolidation
│   │   │
│   │   ├── voice/
│   │   │   ├── voiceService.js       # Voice processing
│   │   │   ├── speechToTextService.js # STT conversion
│   │   │   ├── textToSpeechService.js # TTS conversion
│   │   │   └── voiceCloningService.js # Voice cloning
│   │   │
│   │   ├── blockchain/
│   │   │   ├── blockchainService.js  # Main blockchain service
│   │   │   ├── web3Service.js        # Web3 operations
│   │   │   ├── nftService.js         # NFT operations
│   │   │   ├── contractService.js    # Smart contract calls
│   │   │   └── eventListenerService.js # Blockchain events
│   │   │
│   │   ├── storage/
│   │   │   ├── ipfsService.js        # IPFS operations
│   │   │   ├── fileUploadService.js  # File handling
│   │   │   ├── encryptionService.js  # Data encryption
│   │   │   └── backupService.js      # Data backup
│   │   │
│   │   ├── personality/
│   │   │   ├── personalityService.js # Personality modeling
│   │   │   ├── traitService.js       # Trait management
│   │   │   ├── evolutionService.js   # Personality evolution
│   │   │   └── breedingService.js    # Trait breeding
│   │   │
│   │   └── training/
│   │       ├── trainingService.js    # Core training logic
│   │       ├── skillExtractionService.js # Extract skills
│   │       ├── habitLearningService.js # Learn habits
│   │       └── progressTrackingService.js # Track progress
```

### Middleware & Infrastructure

```
│   ├── middleware/
│   │   ├── auth.js                   # Wallet authentication
│   │   ├── rateLimiter.js           # API rate limiting
│   │   ├── validation.js            # Input validation
│   │   ├── encryption.js            # Request encryption
│   │   ├── cors.js                  # CORS configuration
│   │   ├── errorHandler.js          # Error handling
│   │   └── logging.js               # Request logging
│   │
│   ├── routes/
│   │   ├── agents.js                # /api/agents/*
│   │   ├── training.js              # /api/training/*
│   │   ├── memory.js                # /api/memory/*
│   │   ├── conversation.js          # /api/chat/*
│   │   ├── voice.js                 # /api/voice/*
│   │   ├── breeding.js              # /api/breeding/*
│   │   ├── marketplace.js           # /api/marketplace/*
│   │   ├── users.js                 # /api/users/*
│   │   ├── blockchain.js            # /api/blockchain/*
│   │   └── analytics.js             # /api/analytics/*
```

### Utilities & Background Services

```
│   ├── utils/
│   │   ├── database/
│   │   │   ├── connection.js        # DB connection
│   │   │   ├── migrations.js        # DB migrations
│   │   │   └── seeds.js             # Initial data
│   │   │
│   │   ├── crypto/
│   │   │   ├── encryption.js        # Encryption utilities
│   │   │   ├── hashing.js           # Hashing functions
│   │   │   └── signatures.js        # Digital signatures
│   │   │
│   │   ├── ai/
│   │   │   ├── promptTemplates.js   # AI prompt templates
│   │   │   ├── contextBuilder.js    # Build AI context
│   │   │   ├── responseParser.js    # Parse AI responses
│   │   │   └── tokenizer.js         # Text tokenization
│   │   │
│   │   └── general/
│   │       ├── logger.js            # Logging system
│   │       ├── fileHandler.js       # File operations
│   │       ├── validator.js         # Data validation
│   │       ├── cache.js             # Caching utilities
│   │       └── constants.js         # App constants
│   │
│   ├── jobs/
│   │   ├── memoryConsolidation.js   # Background memory processing
│   │   ├── modelTraining.js         # AI model training jobs
│   │   ├── blockchainSync.js        # Sync blockchain data
│   │   ├── backupData.js            # Data backup jobs
│   │   └── cleanup.js               # Cleanup old data
│   │
│   ├── config/
│   │   ├── database.js              # Database configuration
│   │   ├── ai.js                    # AI service configs
│   │   ├── blockchain.js            # Web3 configurations
│   │   ├── storage.js               # IPFS/storage configs
│   │   ├── redis.js                 # Redis configuration
│   │   ├── server.js                # Server configuration
│   │   └── environment.js           # Environment variables
│   │
│   └── app.js                       # Main Express app
```

### Testing & Development Infrastructure

```
├── tests/
│   ├── unit/
│   │   ├── controllers/
│   │   ├── services/
│   │   └── utils/
│   │
│   ├── integration/
│   │   ├── api/
│   │   ├── blockchain/
│   │   └── database/
│   │
│   └── e2e/
│       ├── agent-lifecycle.test.js
│       ├── training-flow.test.js
│       └── breeding-flow.test.js
│
├── scripts/
│   ├── deployment/
│   │   ├── deploy.js                # Deployment script
│   │   ├── migrate.js               # Database migration
│   │   └── seed.js                  # Seed initial data
│   │
│   ├── maintenance/
│   │   ├── cleanup.js               # Cleanup scripts
│   │   ├── backup.js                # Backup scripts
│   │   └── optimize.js              # Performance optimization
│   │
│   └── development/
│       ├── resetDB.js               # Reset development DB
│       ├── generateTestData.js      # Generate test data
│       └── startLocal.js            # Local development setup
│
├── logs/                            # Application logs
├── uploads/                         # Temporary file uploads
├── .env.example                     # Environment variables template
├── .gitignore
├── Dockerfile
├── docker-compose.yml
├── package.json
└── README.md
```

---

## 4. Blockchain Structure
**Technology Stack:** Solidity + Foundry

### Smart Contract Architecture

```
blockchain/
├── src/
│   ├── core/
│   │   ├── CryptixiaAgent.sol       # Main Agent NFT contract
│   │   ├── AgentFactory.sol         # Agent creation factory
│   │
