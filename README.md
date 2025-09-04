# Pump.fun Comment Bot

A Node.js-based automated comment bot for the pump.fun platform, built on Solana blockchain technology.

## Contact

- Telegram: [Pioneer](https://t.me/hi_3333)

## Video

https://x.com/TakhiSol/status/1963425063904117084

https://x.com/TakhiSol/status/1963427159235506270

## 🚀 Features

- **Automated Wallet Generation**: Creates new Solana keypairs for each session
- **Smart Authentication**: Signs login messages using Ed25519 cryptography
- **Profile Management**: Automatically creates user profiles with randomized usernames
- **Comment Automation**: Posts randomized positive comments to specified token mints
- **Solana Integration**: Built with @solana/web3.js for blockchain operations

## 📁 Project Structure

```
Pumpfun-comment-bot/
├── simple-pump-commenter.js    # Main bot implementation
├── README.md                   # This documentation
└── package.json               # Dependencies (to be created)
```

## 🛠️ Dependencies

- `@solana/web3.js` - Solana blockchain integration
- `tweetnacl` - Cryptography library for Ed25519 signatures
- `bs58` - Base58 encoding/decoding
- `node-fetch` - HTTP client for API requests

## ⚙️ Configuration

### Target Configuration
- **Target Mint**: `GkerzXMnCzcgxE6tGv767r2ySj7SMJoJ9Zx134wUpump`
- **API Base**: `https://frontend-api-v3.pump.fun`
- **Origin**: `https://pump.fun`

### Comment Templates
The bot uses 12 pre-defined positive comment templates that rotate randomly:
- "this is working way better than expected"
- "honestly impressed with how responsive this feels"
- "been testing for a while now and zero issues"
- And 9 more variations...

### Profile Settings
- **Username Prefix**: "Mon" + random 4-character suffix
- **Bio**: "Description here"
- **Profile Image**: IPFS-based placeholder

## 🔧 Setup

1. **Install Dependencies**
   ```bash
   npm install @solana/web3.js tweetnacl bs58 node-fetch
   ```

2. **Run the Bot**
   ```bash
   node simple-pump-commenter.js
   ```

## 📋 How It Works

### 1. Wallet Generation
- Creates a new Solana keypair for each session
- Generates public/private key pair using Ed25519 algorithm

### 2. Authentication
- Signs a timestamped login message with the private key
- Sends authentication request to pump.fun API
- Receives and stores authentication token

### 3. Profile Creation
- Generates random username with "Mon" prefix
- Creates user profile with default bio and image
- Stores username for session

### 4. Comment Posting
- Selects random comment from predefined templates
- Posts comment to specified token mint
- Logs detailed request information for debugging

## 🔐 Security Features

- **Unique Sessions**: Each run generates new wallet credentials
- **Cryptographic Signatures**: Uses Ed25519 for secure authentication
- **No Credential Storage**: Keys are generated fresh each time
- **Randomized Usernames**: Prevents pattern detection

## 📊 API Endpoints

- **POST** `/auth/login` - User authentication
- **POST** `/users` - Profile creation
- **POST** `/replies` - Comment posting

## 🚨 Important Notes

- **Educational Purpose**: This tool is for learning and testing purposes
- **Rate Limiting**: Be mindful of API rate limits
- **Terms of Service**: Ensure compliance with platform terms
- **Responsible Use**: Use ethically and responsibly

## 🐛 Troubleshooting

### Common Issues
1. **Login Failed**: Check network connectivity and API status
2. **Profile Creation Failed**: Verify API endpoint availability
3. **Comment Failed**: Ensure target mint is valid and accessible

### Debug Information
The bot provides detailed logging including:
- Generated wallet addresses
- Authentication status
- Profile creation results
- Full HTTP request details for comments

## 📝 License

This project is provided as-is for educational purposes. Use responsibly and in accordance with applicable terms of service.

## 🤝 Contributing

Feel free to submit issues, feature requests, or improvements to the codebase.

---

**Disclaimer**: This tool is intended for educational and testing purposes. Users are responsible for ensuring compliance with platform terms of service and applicable laws.
