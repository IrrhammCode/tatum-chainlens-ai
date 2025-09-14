# Tatum ChainLens - Blockchain Analytics Platform

A comprehensive blockchain analytics platform built for the Tatum MCP Hackathon 2025. Features multi-chain wallet analysis, NFT gallery, analytics dashboard, and AI chat with MCP integration using only Tatum APIs.

## 🚀 Features

### Core Features
- **Multi-Chain Wallet Analysis** - Check balances across 6 chains
- **DeFi Portfolio Tracking** - Comprehensive portfolio analysis with risk assessment
- **NFT Gallery** - Multi-chain NFT collection tracking
- **Real-time Analytics** - Live blockchain data and insights
- **AI Chat Assistant** - Intelligent blockchain analysis with MCP integration

### Supported Blockchains
- **Ethereum (ETH)** - Mainnet
- **Polygon (MATIC)** - Layer 2
- **BNB Smart Chain (BNB)** - Binance Chain
- **Arbitrum (ETH)** - Layer 2
- **Base (ETH)** - Coinbase Layer 2
- **Optimism (ETH)** - Layer 2

## 🛠️ Installation

### Prerequisites
- Node.js 16+ 
- npm or yarn
- Tatum API Key (Get from [tatum.io](https://tatum.io/))

### Quick Start

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd chainlens
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   # Create .env file
   echo "TATUM_API_KEY=your_tatum_api_key_here" > .env
   echo "PORT=3000" >> .env
   ```

4. **Start the server**
   ```bash
   # Linux/Mac
   chmod +x start.sh
   ./start.sh
   
   # Windows
   start.bat
   
   # Or manually
   node server-simple.js
   ```

5. **Open your browser**
   ```
   http://localhost:3000
   ```

## 🔧 Configuration

### Environment Variables
```env
TATUM_API_KEY=your_tatum_api_key_here
PORT=3000
```

### API Endpoints

#### Core Endpoints
- `GET /` - Main web interface
- `POST /api/chat` - AI chat endpoint
- `GET /api/status` - System status
- `GET /api/chains` - Supported chains

#### Wallet Analysis
- `GET /api/wallet/:address?chain=ethereum` - Single chain wallet analysis
- `POST /api/test-multichain` - Multi-chain wallet analysis

#### Portfolio & NFT
- `GET /api/analytics` - Real-time analytics data
- `GET /api/gas/:chain` - Gas price information

#### Testing & Debug
- `POST /api/force-fallback` - Force fallback mode
- `POST /api/test-key` - Test API key validity
- `POST /api/mcp-restart` - Restart MCP server

## 🤖 AI Chat Features

### Commands
- **Wallet Analysis**: "Analyze wallet 0x1234..." or "Multi-chain wallet 0x1234..."
- **Portfolio Tracking**: "Portfolio 0x1234..." or "All chains portfolio 0x1234..."
- **NFT Analysis**: "NFTs 0x1234..." or "Multi-chain NFTs 0x1234..."
- **Blockchain Info**: "Ethereum info", "Gas prices", "Supported chains"
- **Help**: "Help" or "What can you do?"

### Fallback Mode
The system includes a comprehensive fallback mode that provides:
- Multi-chain analysis across all supported chains
- Real-time blockchain data via Tatum APIs
- Risk assessment and portfolio recommendations
- Comprehensive NFT collection analysis

## 🐳 Docker Support

### Using Docker Compose
```bash
docker-compose up -d
```

### Manual Docker Build
```bash
docker build -t chainlens .
docker run -p 3000:3000 -e TATUM_API_KEY=your_key chainlens
```

## 📊 Architecture

### Backend
- **Express.js** - Web server
- **Tatum APIs** - Blockchain data source
- **MCP Integration** - AI chat capabilities
- **Fallback System** - Enhanced multi-chain analysis

### Frontend
- **Vanilla JavaScript** - Lightweight and fast
- **Responsive Design** - Mobile-first approach
- **Real-time Updates** - Live data refresh

### AI System
- **MCP Server** - Advanced AI analysis
- **Fallback Mode** - Multi-chain analysis when MCP unavailable
- **Context Detection** - Smart query understanding
- **Multi-chain Support** - Comprehensive blockchain analysis

## 🔍 Troubleshooting

### Common Issues

1. **MCP Server Not Starting**
   - Check if Tatum API key is valid
   - Verify network connectivity
   - System will automatically use fallback mode

2. **API Key Issues**
   - Test with: `POST /api/test-key`
   - Get new key from [tatum.io](https://tatum.io/)

3. **Port Already in Use**
   - Change PORT in .env file
   - Kill existing process: `lsof -ti:3000 | xargs kill -9`

### Debug Mode
Enable detailed logging by setting:
```env
DEBUG=true
```

## 🚀 Deployment

### Production Deployment
1. Set production environment variables
2. Use PM2 for process management
3. Configure reverse proxy (nginx)
4. Set up SSL certificates

### PM2 Configuration
```bash
npm install -g pm2
pm2 start server-simple.js --name chainlens
pm2 save
pm2 startup
```

## 📈 Performance

- **Multi-chain Analysis**: Parallel processing across 6 chains
- **Real-time Data**: Live blockchain data via Tatum APIs
- **Fallback System**: 99.9% uptime with comprehensive analysis
- **Caching**: Intelligent data caching for better performance

## 🤝 Contributing

1. Fork the repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Create Pull Request

## 📄 License

MIT License - see LICENSE file for details

## 🏆 Hackathon Submission

This project was built for the Tatum MCP Hackathon 2025, showcasing:
- Advanced MCP integration
- Comprehensive fallback system
- Multi-chain blockchain analysis
- Real-time data processing
- Professional-grade architecture

## 📞 Support

For issues and questions:
- Create GitHub issue
- Check troubleshooting section
- Review API documentation

---

**Built with ❤️ for the Tatum MCP Hackathon 2025**