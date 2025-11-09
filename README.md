# Scavenger Miner - Profit-Sharing Mining Tool

A high-performance, multi-threaded mining tool for Scavenger Mine that mines directly to **YOUR OWN WALLETS**. No wallet creation, no private key exposure - just pure mining power for your registered addresses.

## 🎯 Why Choose This Miner?

### ✅ YOUR KEYS, YOUR WALLET - Complete Control
Unlike other mining tools that create new wallets and control your private keys, this miner:
- ✅ Mines directly to **your existing wallet addresses**
- ✅ **Never asks for private keys** - only wallet addresses needed
- ✅ No risk of key theft or unauthorized access
- ✅ You maintain complete control of your assets

### 🚀 Advanced Features
- **Auto-Retry System** - Failed submissions are automatically retried after 1 hour (wallet not registered, server overload, rate limiting, etc.)
- **Multi-Core Mining** - Utilizes multiple CPU threads to maximize solution discovery
- **Crypto Receipt Storage** - All solutions saved with receipts in `solutions/` folder for dispute resolution
- **Verifiable Solutions** - Check your submitted solutions on [Scavenger Mine website](https://sm.midnight.gd/wizard/mine)
- **Smart Challenge Selection** - Auto-solves previous challenges when current ones are completed
- **Interactive & CLI Modes** - Easy for beginners, powerful for advanced users
- **One-Click Setup** - No installation required, just download and run
- **Higher Success Rate** - More solutions than browser mining, no session restarts needed

## 💰 Profit Sharing - 8% Fee (92% to You!)

This miner operates on a transparent profit-sharing model:
- **User gets: 11 solutions out of every 12 (91.67%)**
- **Owner gets: 1 solution out of every 12 (8.33%)**

Example: If you find 120 solutions, you get 110 and the owner gets 10.

## 📋 System Requirements

- **OS**: Windows 10/11, Linux (Ubuntu 20.04+), or macOS (10.15+)
- **CPU**: Multi-core processor (recommended: 2+ cores)
- **RAM**: 3GB minimum, 8GB recommended
- **Storage**: 2GB free space
- **Network**: Stable internet connection

## 🚀 Quick Start Guide

### Step 1: Register Your Wallet
⚠️ **IMPORTANT**: Before using this miner, you **MUST** register your wallet addresses for the Scavenger Mine airdrop at:
👉 **https://sm.midnight.gd/wizard/mine**

This miner only solves and submits solutions - it does NOT register wallets for you. Hence it doesn't need to know your private keys.

### Step 2: Download the Miner

Download the appropriate version for your operating system:

- **Windows**: `scavenger-miner.exe`
- **Linux**: `scavenger-miner`
- **macOS**: `scavenger-miner-universal`


### Step 3: Prepare Your Wallets File

Create a file named `wallets.txt` in the same folder as the miner executable.

Add your registered wallet addresses, **one address per line**:

```
wallet_address_1
wallet_address_2
wallet_address_3
```

For example:

```
addr1qxf6n6ulf6el4rg5d9429c6265pykgezprnsdg5pkp4chfyl9fufw6c0tc47ycz24hudr0fl4pwx7pyhzzgm20utnw3sctf57r
addr1qx25lz6le9qsyuqjmnml4jsc8v85p3suhjha4v6x93vfqgmjqgzwp43jngg5yea289p56gu30lv5hfh65x5ej7ymfqkqcruae6
addr1qydfg5p9vw9ev2v4cx6ak2pmt9xrfav6qj2zz8gg6stdwj48sczdgxveldgl9zqkkq73kchquu7h3wyltnwxynkffx6qd43xst
```

### Step 4: Run the Miner

#### Windows
Double click on the scavenger-miner.exe file, or run the following command in Command Prompt / PowerShell
```bash
scavenger-miner.exe
```

#### Linux/macOS
```bash
chmod +x scavenger-miner  # First time only (macOS: scavenger-miner-universal)
./scavenger-miner
```


#### Interactive Mode (Recommended for Beginners)

The miner will ask you:

1. **Wallets file location**
   - If `wallets.txt` is in the same folder: Just press **Enter**
   - Otherwise: Type the full path to your `wallets.txt` file

2. **CPU usage percentage** (10-100%)
   - Press **Enter** for default: 50%
   - Or type a number: e.g., `70` for 70% of CPU cores
   - ⚠️ Start with 50%, increase gradually if needed

3. **Discount code** (optional - for community members only)
   - Community members: Enter your code
   - Global users: Just press **Enter** to skip

#### Command-Line Mode (For Advanced Users who want to run the miner on background or as a systemd service)

Syntax: `executable_name location_to_wallets_file CPU_percentage`

**Windows:**
```bash
scavenger-miner.exe wallets.txt 70
```

**Linux:**
```bash
./scavenger-miner wallets.txt 70
```

**macOS:**
```bash
./scavenger-miner-universal wallets.txt 70
```

Examples:
- Use default 50% CPU: `./scavenger-miner wallets.txt 50`
- Use 80% CPU: `./scavenger-miner wallets.txt 80`
- Custom wallet file path: `./scavenger-miner /path/to/wallets.txt 60`

## 📊 Verifying Your Solutions

1. Visit https://sm.midnight.gd/wizard/mine
2. Connect your wallet address
3. Check "Your submitted solutions:" counter
4. **DO NOT** start mining session in the browser while using this tool
5. Refresh the page to see updated solution counts after running this tool for a while

## ⚠️ Important Warnings

### CPU Usage Guidelines
- ⚠️ **Start with 50% of your CPU cores** and monitor system performance
- ⚠️ **Don't exceed 80% CPU usage** unless using a dedicated server
- ⚠️ High CPU usage may slow down other applications and increase electricity costs
- ⚠️ Monitor temperatures to prevent overheating

### Avoid Solution Conflicts
- ❌ **DO NOT mine the same wallet** in both browser and this tool simultaneously
- ❌ One method finding the solution first makes the other's work wasted
- ✅ Choose one method per wallet address

### Preserve Your Solutions
- 📁 **DO NOT delete the `solutions/` folder** after using this tool
- 📁 This folder contains all your solutions and crypto receipts
- 📁 You may need these records for dispute resolution with Scavenger Mine

## 📁 Output Files

The miner creates two directories:

- **`solutions/`** - JSON files with all found solutions and crypto receipts
- **`logs/`** - Mining session logs with timestamps

Keep these folders safe for your records!

## 🎥 Video Tutorial

*Video guide will be added here*

## 📸 User Testimonials

*Screenshots and feedback from users will be added here*

## ❓ Frequently Asked Questions

**Q: Do I need to provide my private keys?**  
A: **NO!** This miner only needs your wallet addresses. Never share your private keys with anyone.

**Q: What happens if a solution submission fails?**  
A: The miner automatically retries failed submissions after 1 hour. All solutions are saved in the `solutions/` folder.

**Q: Can I use multiple wallets?**  
A: Yes! You can mine for multiple wallet addresses simultaneously. Just put your wallet addresses in the wallets.txt file, one address per line. 

**Q: What's the discount code for?**  
A: The discount code is exclusively for our community members. Global users can skip this by pressing Enter.

**Q: How do I know if my solutions are submitted?**  
A: Check the `solutions/` folder for crypto receipts, or verify on the Scavenger Mine website by connecting your wallet.

**Q: Can I run this on a VPS?**  
A: Yes! Use command-line mode for VPS deployment. See the Advanced section above.

**Q: Is this better than browser mining?**  
A: Yes! This miner achieves higher solution rates, uses multiple CPU cores efficiently, and doesn't require session restarts.

**Q: What if my wallet isn't registered?**  
A: Solutions will fail initially (with error message "Solution validation failed: Address is not registered") but will be auto-retried every hour, make sure to register your wallet addresses in 24 hours to avoid the expiration of the solution. Always register at https://sm.midnight.gd/wizard/mine first.

**Q: How much CPU should I use?**  
A: Start with 50% of your cores. Monitor performance and gradually increase if needed, but stay under 80% for non-dedicated machines.

**Q: Can I trust this miner with my wallets?**  
A: This miner **never asks for private keys** - only addresses. You can verify this is safe because it only needs your public wallet address to submit solutions.

## 📞 Support & Contact

For support, questions, or feedback:
- **GitHub Issues**: [Open an issue](../../issues)

## 📜 License

This software is provided as-is. Use at your own risk. Always follow Scavenger Mine's terms of service.

---

**Happy Mining! 🚀⛏️**

*Remember: YOUR KEYS, YOUR WALLET - Mine safely and profitably!*
