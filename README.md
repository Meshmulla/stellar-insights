# Ndii Intelligence Dashboard

**A Stellar Analytics Engine that quantifies payment reliability and liquidity health — so wallets, apps, and anchors can make payments with confidence.**

[![React](https://img.shields.io/badge/React-18-blue)](https://react.dev) [![TypeScript](https://img.shields.io/badge/TypeScript-5.8-blue)](https://www.typescriptlang.org) [![Vite](https://img.shields.io/badge/Vite-5.4-blueviolet)](https://vitejs.dev) [![Stellar](https://img.shields.io/badge/Stellar-Network-brightgreen)](https://stellar.org)

---

## 🎯 The Problem

Stellar is widely used for **stablecoins, cross-border payments, asset issuance, and remittances**, but *speed alone isn't enough* — **payment reliability and liquidity health are real challenges**:

- 📉 **Which asset corridors consistently succeed vs fail?**
- 💧 **Is there enough liquidity in major payment paths?**
- ⚓ **Are certain anchors or assets bottlenecks in transfers?**
- 📊 **Are markets efficient, stable, or unreliable under stress?**

**Current tools** show raw transactions; few show *how well payments actually work in practice*.

---

## 💡 The Solution

Ndii Intelligence Dashboard provides **deep insights into Stellar payment network performance**, enabling wallets, developers, businesses, and anchors to:

✅ **Predict payment success likelihood** before sending  
✅ **Optimize routing paths** for reliability  
✅ **Quantify real-world payment reliability** (not just TPS)  
✅ **Identify liquidity bottlenecks** and improve provisioning  
✅ **Understand ecosystem risk** and health trends  

---

## 📊 What You Get

### 🎯 Core Intelligence Features

| Feature | Impact |
|---------|--------|
| **Payment Reliability Metrics** | % successful vs attempted payments across corridors |
| **Corridor Health Scoring** | Average slippage, bid-ask spread, liquidity depth analysis |
| **Anchor Performance Tracking** | Weighted reliability scores and failure rate monitoring |
| **Liquidity Dynamics** | TVL trends, active liquidity over time, stress testing |
| **Payment Latency Analysis** | Median confirmation times and settlement speed trends |
| **Heatmap Visualization** | See which asset pairs and corridors are most/least reliable |

### 🛣️ Key Pages

**📈 Dashboard**
- Real-time KPIs: Success rate, active corridors, liquidity depth, settlement speed
- Payment volume trends and patterns
- Corridor reliability heatmap
- Top performing assets ranking

**🛣️ Corridors Page**
- Deep dive into payment corridors (asset pair routes)
- Success rate and slippage metrics
- Volume trends and historical analysis
- Identify fragile vs robust routing paths

**⚓ Anchors Page**
- Anchor/issuer reliability scorecards
- Asset portfolio per anchor
- Transaction success rates and failure monitoring
- Health status indicators (green/yellow/red)

---

## 👥 Who Benefits

| User Type | Value |
|-----------|-------|
| **Wallets & Apps** | Predict payment success before sending; suggest optimal routes |
| **Businesses & Remittance Services** | Avoid failed transactions; build reliable payment infrastructure |
| **Anchors & Issuers** | See liquidity provisioning gaps; prioritize high-adoption markets |
| **DeFi Builders** | Understand ecosystem efficiency and routing reliability |
| **Compliance & Regulators** | Spot congested corridors; assess ecosystem risk |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────┐
│                  Frontend (React + TS)                  │
│  Dashboard | Corridors | Anchors | Analytics            │
└──────────────────┬──────────────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────────────┐
│           API Layer (REST Endpoints)                    │
│   /payments | /corridors | /anchors | /liquidity        │
└──────────────────┬──────────────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────────────┐
│         Metrics Engine & Data Processing                │
│   Success Scoring | Corridor Analysis | Liquidity       │
└──────────────────┬──────────────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────────────┐
│            Data Layer & Indexing                        │
│   Stellar RPC | Historical DB | Order Books             │
└─────────────────────────────────────────────────────────┘
```

---

## 🚀 Tech Stack

**Frontend**
- React 18 with TypeScript for type-safe components
- Vite 5 for lightning-fast builds
- shadcn-ui for consistent, accessible UI components
- Tailwind CSS for responsive design
- Recharts for financial data visualization

**State & Data**
- TanStack React Query for efficient data fetching
- React Router v6 for seamless navigation
- React Hook Form + Zod for validated forms

**Developer Experience**
- TypeScript for type safety
- ESLint for code quality
- Vitest + React Testing Library for testing
- Hot module reloading during development

---

## 🎬 Getting Started

### Prerequisites

- Node.js 18+ ([install with nvm](https://github.com/nvm-sh/nvm))
- Bun or npm/yarn

### Quick Start

```bash
# Clone the repository
git clone https://github.com/Ndifreke000/stellar-insights.git
cd stellar-insights

# Install dependencies
bun install

# Start development server
bun dev
```

The app will be available at `http://localhost:5173`

### Available Commands

```bash
bun dev              # Start dev server with HMR
bun run build        # Production build
bun run build:dev    # Development build
bun run preview      # Preview production build
bun run test         # Run tests
bun run test:watch   # Watch mode testing
bun run lint         # Code quality check
```

---

## 📁 Project Structure

```
stellar-insights/
├── src/
│   ├── pages/                # Main pages (Dashboard, Corridors, Anchors)
│   ├── components/
│   │   ├── dashboard/        # Dashboard visualizations
│   │   ├── layout/           # Navigation & layout
│   │   └── ui/               # Reusable shadcn-ui components
│   ├── data/
│   │   └── mockData.ts       # Mock metrics (ready for real API)
│   ├── hooks/                # React hooks (toast, mobile)
│   ├── lib/                  # Utilities
│   └── App.tsx               # Router configuration
├── public/                   # Static assets
├── vite.config.ts            # Vite configuration
├── tailwind.config.ts        # Tailwind theming
├── tsconfig.json             # TypeScript config
└── package.json              # Dependencies
```

---

## 📊 Core Metrics Explained

### Payment Reliability
Percentage of payments that successfully settle vs total attempted:
- Tracks corridor-specific success patterns
- Identifies failure-prone routes
- Helps predict payment outcomes

### Corridor Health Score
Composite metric measuring efficiency of asset pair routes:
- **Liquidity Depth**: Order book capacity for smooth trades
- **Slippage**: Price impact of trades (lower is better)
- **Success Rate**: Percentage of successful trades
- **Latency**: Median settlement time

### Anchor Performance Index
Reliability scoring for asset issuers:
- Success rate of transactions
- Failure frequency and patterns
- Asset diversity and adoption
- Health status (green/yellow/red)

### Liquidity Dynamics
Understanding of capital flow and availability:
- Total Value Locked (TVL) trends
- Active liquidity movements
- Stress testing scenarios
- Temporal patterns (peak vs off-peak)

---

## 🔌 Data Integration Ready

The dashboard uses mock data but is built to integrate with:

**Stellar RPC**
- Real-time ledger data
- Payment and transaction history
- Order book snapshots

**Data Indexing Services**
- Historical payment flow analysis
- Bitquery or similar indexing tools
- Custom event tracking

**Future Enhancements**
- Live data streaming
- Predictive analytics
- Alert systems
- Export capabilities

See [ARCHITECTURE.md](./docs/ARCHITECTURE.md) for data integration details.

---

## 📈 MVP Scope & Roadmap

### Phase 1: Foundation (Current)
- [x] Dashboard infrastructure
- [x] Core UI components
- [x] Corridor analysis
- [x] Anchor tracking
- [x] Mock data structure

### Phase 2: Real Data Integration
- [ ] Stellar RPC integration
- [ ] Historical data indexing
- [ ] Real payment metrics
- [ ] Live liquidity feeds

### Phase 3: Advanced Analytics
- [ ] Predictive success scoring
- [ ] Optimal routing engine
- [ ] Alert system
- [ ] Custom reports

### Phase 4: Scale & Optimize
- [ ] Performance optimization
- [ ] Mobile-first improvements
- [ ] Advanced filtering
- [ ] Data export

---

## 🤝 Contributing

We welcome contributions! Here's how to get started:

```bash
# Create a feature branch
git checkout -b feature/your-feature

# Make your changes and commit
git commit -am "feat: describe your changes"

# Push and open a PR
git push origin feature/your-feature
```

**Guidelines:**
- Follow TypeScript best practices
- Ensure tests pass: `bun run test`
- Lint your code: `bun run lint`
- Add tests for new features

---

## 🚀 Deployment

### Build for Production
```bash
bun run build
```

Output goes to `dist/` directory.

### Deploy to Vercel (Recommended)
```bash
# Vercel auto-detects Vite
# Just connect your GitHub repo
```

### Other Platforms
- **Netlify** – Drag & drop `dist/` folder
- **AWS S3 + CloudFront** – Perfect for static SPA
- **Firebase Hosting** – Connect GitHub repo
- **GitHub Pages** – Simple static hosting

---

## 📖 Documentation

- [FEATURES.md](./docs/FEATURES.md) – Detailed feature documentation
- [ARCHITECTURE.md](./docs/ARCHITECTURE.md) – System design & data flow
- [CONTRIBUTING.md](./CONTRIBUTING.md) – Development guidelines
- [API.md](./docs/API.md) – Endpoints & data structures

---

## 📊 Key Metrics At a Glance

**Current Dashboard Data (Example)**
- ✅ **Payment Success Rate**: 97.8%
- 🛣️ **Active Corridors**: 142 asset pair routes
- 💧 **Liquidity Depth**: $847.5M total
- ⚡ **Avg Settlement**: 4.2 seconds
- 📈 **7-Day Volume Trend**: Growing

---

## 🔗 Resources

- [Stellar Documentation](https://developers.stellar.org)
- [Stellar RPC API](https://developers.stellar.org/docs/data/apis/rpc)
- [Stellar Network Stats](https://stellar.expert)
- [Create React App Docs](https://react.dev)

---

## 📄 License

[Specify your license - e.g., MIT, Apache 2.0]

---

## 🎓 Portfolio Impact

**This project demonstrates:**
- Full-stack architecture thinking (frontend → API → data)
- Financial metrics & analytics design
- Real-world problem solving (payment reliability)
- Production-grade React/TypeScript practices
- Stellar ecosystem knowledge
- UI/UX for complex data visualization

**Great talking points for:**
- FinTech roles
- Blockchain/Web3 positions
- Data analytics engineering
- Product management interviews

---

## 📞 Support

For issues, questions, or suggestions:
- Open an [issue](https://github.com/Ndifreke000/stellar-insights/issues)
- Check [existing discussions](https://github.com/Ndifreke000/stellar-insights/discussions)
- Email: [your email]

---

**Built with ❤️ for the Stellar ecosystem**
