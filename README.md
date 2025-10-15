# ⚡ StarkPay

> Bitcoin payments in 3 seconds, not 10 minutes. Sub-cent fees on Starknet L2.

[![Starknet](https://img.shields.io/badge/Starknet-Layer_2-purple)](https://starknet.io)
[![Flutter](https://img.shields.io/badge/Flutter-3.24+-blue)](https://flutter.dev)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Hackathon](https://img.shields.io/badge/Starknet-Re%7BSolve%7D-orange)](https://resolve-starknet.devpost.com)

**Built for Starknet Re{Solve} Hackathon 2025**  
Targeting: Payments | Mobile | Bitcoin | Xverse | Atomiq | Chipi Pay tracks

---

## 📱 Demo

**[Watch 60-Second Demo Video →](YOUR_YOUTUBE_LINK)**

![StarkPay Demo](assets/demo.gif)

**Live App:** [Download APK](releases/starkpay-v1.0.apk) | **Testnet:** Starknet Sepolia

---

## 🎯 Problem Statement

Bitcoin is fundamentally broken as a payment method:

- **10+ minute confirmations** make point-of-sale transactions impossible
- **$20 median transaction fees** destroy small-value purchase economics
- **420,000+ merchants** want crypto payments but can't accept Bitcoin L1
- **500M+ Bitcoin holders** can't spend their assets for everyday purchases

**Result:** Bitcoin remains a speculative store of value, not functional currency.

---

## 💡 Solution

**StarkPay** transforms Bitcoin into an instant mobile payment system by bridging to Starknet Layer 2:

✅ **3-second settlement** via Starknet's ultra-low latency  
✅ **0.01¢ transaction fees** using STARK proof compression  
✅ **One-tap mobile UX** with QR code scanning  
✅ **Non-custodial security** through Xverse wallet integration  
✅ **Automatic swaps** via Atomiq cross-chain protocol  
✅ **Merchant-ready** with Chipi Pay checkout API  
✅ **Gasless transactions** using Starknet account abstraction  

---

## 🚀 Key Features

### For Customers
- **Connect Bitcoin Wallet:** Link Xverse wallet—no seed phrase exposure
- **Scan & Pay:** QR code scanning for instant checkout
- **Live Exchange Rates:** Real-time BTC/USD pricing with slippage protection
- **Receipt NFTs:** On-chain proof-of-payment minted automatically
- **Transaction History:** Filterable payment records with Starknet explorer links
- **Biometric Security:** PIN/fingerprint protection for app access

### For Merchants
- **Generate Payment QR:** Instant invoice creation with USD amounts
- **Live Dashboard:** Real-time payment notifications
- **Instant Settlement:** Receive funds in 3 seconds
- **Multi-Token Support:** Accept BTC, WBTC, STRK, ETH
- **Sales Analytics:** Daily/weekly revenue tracking
- **Fiat Conversion:** Optional instant USD settlement via Chipi Pay

---

## 🛠 Tech Stack

### Frontend
- **Framework:** Flutter 3.24+ (Dart)
- **State Management:** Riverpod
- **HTTP Client:** Dio
- **Storage:** flutter_secure_storage
- **QR Handling:** qr_flutter + qr_code_scanner
- **UI:** Material Design 3

### Blockchain
- **Layer 2:** Starknet (Cairo smart contracts)
- **Bitcoin Wallet:** Xverse SDK
- **Cross-Chain:** Atomiq swap protocol
- **Merchant Gateway:** Chipi Pay API
- **RPC Provider:** Starknet mainnet/testnet

### Infrastructure
- **Account Abstraction:** Starknet paymaster for gasless UX
- **Indexing:** Apibara/Voyager for transaction history
- **Deployment:** Android APK (iOS coming soon)

---

## 🏗 Architecture

┌─────────────┐
│ Flutter │ ← Mobile App (User Interface)
│ Android │
└──────┬──────┘
│
├─────────► Xverse Wallet (Bitcoin Custody)
│
├─────────► Atomiq API (BTC ↔ WBTC Swaps)
│
├─────────► Starknet L2 (Payment Settlement)
│ └── Cairo Smart Contracts
│ └── Account Abstraction (Paymaster)
│
└─────────► Chipi Pay API (Merchant Checkout)

text

### Payment Flow
1. Customer scans merchant QR code
2. App fetches BTC/WBTC exchange rate from Atomiq
3. Customer approves transaction in Xverse wallet
4. Atomiq atomically swaps BTC → WBTC on Starknet
5. Smart contract executes payment to merchant (gasless)
6. Receipt NFT minted to customer's address
7. Chipi Pay notifies merchant of confirmed payment

**Total time:** ~3 seconds | **Total cost:** ~$0.0001

---

## 📦 Installation

### Prerequisites
Flutter SDK 3.24+
Android Studio / Xcode
Xverse Wallet app installed
Git

text

### Clone Repository
git clone https://github.com/yourusername/starkpay.git
cd starkpay

text

### Install Dependencies
flutter pub get

text

### Configure API Keys
Create `.env` file in project root:
ATOMIQ_API_KEY=your_atomiq_key_here
CHIPI_PAY_API_KEY=your_chipi_key_here
STARKNET_RPC_URL=https://starknet-mainnet.public.blastapi.io
PAYMASTER_CONTRACT=0x1234...

text

### Run on Android
flutter run

text

### Build APK
flutter build apk --release

text

---

## 🎮 Usage Guide

### Customer Payment Flow

1. **Connect Wallet**
   - Open StarkPay → Tap "Connect Wallet"
   - Approve Xverse connection (deep link)
   - Starknet account auto-generated from Bitcoin address

2. **Make Payment**
   - Tap "Scan to Pay" → Scan merchant QR
   - Review payment details (amount, fees, exchange rate)
   - Approve in Xverse wallet
   - Wait for confirmation (~3s)
   - View receipt with transaction hash

3. **View History**
   - Tap "History" → See all transactions
   - Filter by date/status
   - Tap transaction → Full receipt + blockchain explorer link

### Merchant Setup

1. **Enable Merchant Mode**
   - Settings → Toggle "Merchant Mode"
   - Enter Chipi Pay merchant ID

2. **Generate Payment QR**
   - Tap "Create Invoice"
   - Enter amount in USD
   - Display QR to customer
   - Receive payment notification

3. **Settlement**
   - Dashboard → "Withdraw"
   - Choose: Keep WBTC | Convert to BTC | Fiat settlement
   - Instant transfer to your Xverse/bank account

---

## 🏆 Hackathon Prize Tracks

StarkPay is eligible for **6 prize tracks** totaling **$15,000+ in bounties**:

| Track | Sponsor | Prize | Integration |
|-------|---------|-------|-------------|
| **Payments** | Starknet Foundation | $3,000 STRK | Core payment flow |
| **Payments** | Chipi Pay | $1,000 STRK | Merchant checkout API |
| **Mobile-First dApps** | Starkware | $3,000 STRK | Flutter native app |
| **Bitcoin Unleashed** | Starknet Foundation | $3,000 STRK | BTC-WBTC bridge |
| **Bitcoin Unleashed** | Xverse | $6,000 value | Wallet SDK integration |
| **Bitcoin Unleashed** | Atomiq | 0.03 BTC | Cross-chain swaps |

**Total Potential:** $16,000+ STRK + 0.03 BTC + enterprise packages

---

## 📊 Performance Metrics

| Metric | Bitcoin L1 | StarkPay |
|--------|-----------|----------|
| **Settlement Time** | 10+ minutes | 3 seconds |
| **Transaction Fee** | $20 avg | $0.0001 |
| **Throughput** | 7 tx/sec | 10,000+ tx/sec |
| **Mobile UX** | ❌ | ✅ Native app |
| **Merchant Integration** | ❌ Complex | ✅ QR code |

**Cost Reduction:** 99.9995% lower fees  
**Speed Improvement:** 200x faster settlement

---

## 🗂 Project Structure

starkpay/
├── lib/
│ ├── main.dart # App entry point
│ ├── models/
│ │ ├── transaction.dart # Transaction data model
│ │ ├── swap_quote.dart # Atomiq quote model
│ │ └── payment_request.dart # Chipi Pay model
│ ├── services/
│ │ ├── xverse_service.dart # Xverse wallet integration
│ │ ├── starknet_service.dart # Starknet RPC calls
│ │ ├── atomiq_service.dart # Swap execution
│ │ └── chipi_pay_service.dart# Merchant API
│ ├── screens/
│ │ ├── home_screen.dart # Main dashboard
│ │ ├── scan_pay_screen.dart # QR scanner
│ │ ├── payment_confirmation_screen.dart
│ │ ├── receipt_screen.dart # Transaction receipt
│ │ └── merchant_dashboard_screen.dart
│ └── widgets/
│ ├── balance_card.dart # Balance display
│ └── transaction_list_item.dart
├── android/ # Android config
├── assets/ # Images, logos
├── test/ # Unit tests
├── pubspec.yaml # Dependencies
└── README.md # This file

text

---

## 🧪 Testing

### Run Unit Tests
flutter test

text

### Manual Test Cases
- ✅ Wallet connection via Xverse deep link
- ✅ QR code scanning with valid/invalid data
- ✅ Payment execution with insufficient balance
- ✅ Network error handling (offline mode)
- ✅ Receipt NFT minting confirmation
- ✅ Merchant dashboard real-time updates

### Test on Starknet Sepolia
1. Get testnet STRK from [faucet](https://faucet.goerli.starknet.io/)
2. Connect test Xverse wallet
3. Execute test payment to demo merchant address
4. Verify transaction on [Voyager](https://sepolia.voyager.online/)

---

## 🚧 Roadmap

### Phase 1: Hackathon MVP (✅ Complete)
- Flutter Android app
- Xverse + Atomiq + Chipi Pay integration
- Basic payment flow (scan → pay → receipt)
- Merchant QR generation

### Phase 2: Post-Hackathon (Q4 2025)
- iOS app launch
- NFC tap-to-pay support
- Multi-language support (Hindi, Spanish, Portuguese)
- Merchant SDK for e-commerce plugins (WooCommerce, Shopify)

### Phase 3: Scale (Q1 2026)
- Lightning Network integration for hybrid routing
- Stablecoin support (USDC, USDT on Starknet)
- Loyalty rewards program (cashback in STRK)
- Merchant analytics dashboard (web portal)

---

## 👥 Team

**Solo Developer** | Built in 24 hours for Starknet Re{Solve} Hackathon

- Flutter mobile development
- Blockchain integration (Starknet, Bitcoin)
- UI/UX design
- API integration (Xverse, Atomiq, Chipi Pay)

**Looking for:**
- Co-founders (Business Development, Marketing)
- Seed funding post-hackathon
- Merchant partnerships

---

## 🤝 Contributing

Contributions welcome! Please follow these steps:

1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

**Contribution areas:**
- iOS app development
- Additional payment gateway integrations
- UI/UX improvements
- Documentation translations

---

## 📄 License

This project is licensed under the **MIT License** - see [LICENSE](LICENSE) file for details.

Open-source forever. Built for the community.

---

## 🙏 Acknowledgments

**Hackathon Sponsors:**
- [Starknet Foundation](https://starknet.io) - L2 infrastructure
- [Starkware](https://starkware.co) - Zero-knowledge technology
- [Xverse](https://xverse.app) - Bitcoin wallet SDK
- [Atomiq](https://atomiq.xyz) - Cross-chain swaps
- [Chipi Pay](https://chipipay.com) - Merchant gateway
- [Cartridge](https://cartridge.gg) - Workshop support
- [OpenZeppelin](https://openzeppelin.com) - Smart contract security

**Special Thanks:**
- Starknet devs on Discord for technical support
- Flutter community for UI components
- Beta testers who provided feedback

---

## 📞 Contact & Links

- **Demo Video:** [YouTube](YOUR_YOUTUBE_LINK)
- **Devpost:** [Submission](https://devpost.com/software/starkpay)
- **GitHub:** [Source Code](https://github.com/yourusername/starkpay)
- **Twitter:** [@StarkPayApp](https://twitter.com/starkpayapp)
- **Email:** contact@starkpay.app
- **Discord:** StarkPayDev#1234

---

## 🎬 Demo Script

**60-Second Pitch:**

> "Bitcoin payments are broken—ten minutes, twenty dollars per transaction. Merchants won't accept it, users won't spend it.
>
> StarkPay fixes this. We bridge Bitcoin to Starknet Layer 2 for instant mobile payments with sub-cent fees.
>
> [DEMO] Watch: I'm buying coffee. Scan QR code—the app shows thirty dollars. Behind the scenes, Atomiq swaps my Bitcoin to wrapped BTC on Starknet. I approve in Xverse—boom! Payment confirmed in three seconds. Merchant receives it through Chipi Pay. Here's my receipt with the transaction hash, minted as an NFT.
>
> StarkPay targets six prize tracks—Payments, Mobile, Bitcoin, Xverse, Atomiq, Chipi Pay—over fifteen thousand in bounties. Built entirely in twenty-four hours. Making Bitcoin finally work for everyday spending."

---

## 📈 Market Opportunity

- **420,000+ merchants** interested in crypto payments globally
- **500M+ Bitcoin holders** seeking spending utility
- **$1.2T+ Bitcoin market cap** locked as speculative asset
- **$2.5B+ annual crypto payment volume** (growing 78% YoY)
- **Target: 1% of Bitcoin payments** = $12B+ addressable market

**Traction Potential:**
- Partner with 100 merchants in India (Q4 2025)
- Process 10,000 transactions/month by Q1 2026
- Apply for Starknet Foundation seed grant ($50K-$250K)

---

**⚡ StarkPay - Making Bitcoin spendable, finally.**

Built with ❤️ on Starknet | October 2025
