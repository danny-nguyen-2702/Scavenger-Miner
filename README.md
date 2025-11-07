# Scavenger Miner

**High-performance CPU miner for Midnight blockchain's NIGHT token distribution**

[![License: MIT OR Apache-2.0](https://img.shields.io/badge/License-MIT%20OR%20Apache--2.0-blue.svg)](LICENSE)
[![Platform: Windows | macOS | Linux](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey.svg)]()
[![Rust](https://img.shields.io/badge/Rust-1.70%2B-orange.svg)](https://www.rust-lang.org)

Mine NIGHT tokens during the Scavenger Mine phase - no installation required, just download and run!

---

## 🎯 What is Scavenger Miner?

Scavenger Miner is a standalone executable that allows you to participate in the Midnight blockchain's Scavenger Mine token distribution phase. It's designed to be:

- **Simple** - Download and run, no installation needed
- **Fast** - Multi-threaded mining using 50% of your CPU
- **Fair** - ASIC-resistant algorithm (AshMaize) optimized for standard CPUs
- **Safe** - Open source, no admin rights required
- **Automatic** - Fetches tasks and submits solutions automatically

---

## ⚡ Quick Start

### 1. Download

Get the latest release for your platform:

- **Windows:** [scavenger-miner-windows-v1.0.0.zip](https://github.com/danny-nguyen-2702/scavenger-miner/releases/latest)

### 2. Extract

Unzip the downloaded file to any folder.

### 3. Run

**Windows:** Double-click `scavenger-miner.exe`

**macOS:**
```bash
chmod +x scavenger-miner
./scavenger-miner
```

**Linux:**
```bash
chmod +x scavenger-miner
./scavenger-miner
```

That's it! Mining starts automatically.

---

## 📋 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **CPU** | 2 cores | 4+ cores |
| **RAM** | 4 GB | 8 GB |
| **Disk** | 2 GB free | 5 GB free |
| **Internet** | Stable connection | Wired/fast WiFi |

**Supported Platforms:**
- Windows 10/11 (x64)
- macOS 10.15+ (Intel & Apple Silicon)
- Linux (Ubuntu 20.04+, Debian 11+, Fedora 35+, etc.)

---

## 📊 Features

### ✅ Zero Installation
- Download, extract, and run
- No dependencies to install
- No admin/root privileges required
- Works immediately out of the box

### ⚡ High Performance
- Multi-threaded mining (uses 50% of CPU cores by default)
- ROM caching for improved efficiency
- Optimized for x86_64 and ARM64 architectures
- Expected hash rates:
  - Entry laptops: 10-30 H/s
  - Modern laptops: 30-80 H/s
  - Desktop PCs: 50-150 H/s
  - Workstations: 150-300+ H/s

### 🤖 Fully Automatic
- Automatic task fetching from Scavenger Mine API
- Automatic solution submission
- ROM reuse when possible (saves time)
- Continuous operation with retry logic

### 🔒 Safe & Secure
- No personal data collection
- No private keys required (uses public wallet addresses only)
- Statically linked (no system dependencies)

### 🎛️ Smart Resource Management
- Uses 50% of CPU cores by default
- Automatic memory management
- Cooperative threading for optimal performance
- Low system impact - use your computer normally while mining

---

## 📖 Documentation

**Full documentation available:**

- 📘 **[User Manual](USER_MANUAL.md)**
  - Installation instructions
  - Usage guide
  - Troubleshooting
  - FAQ
  - Performance optimization

---

## 🚀 Usage

### Basic Usage

Simply run the executable. The miner will:
1. Connect to Scavenger Mine API
2. Fetch available mining tasks
3. Initialize ROM (takes 2-4s first time)
4. Start mining with multiple threads
5. Automatically submit solutions when found
6. Repeat continuously

### Expected Output

```
╔════════════════════════════════════════════════╗
║   Scavenger Mine AshMaize Miner v4.1          ║
║   Cooperative Threading + ROM Reuse            ║
╚════════════════════════════════════════════════╝

Miner ID: miner-rust-yourcomputer-1730000000
System: 8 vCPUs, using 4 mining threads (50%)

Fetching new task from API...
✓ Fetched task: **D07C10 for addr_test1qq4dl3nhr0...

🔄 ROM cache miss - initializing new ROM...
   ✓ ROM initialized in 45.23s

🚀 Starting 4 mining threads...
[Progress] Total hashes checked: 10000
```

### Stopping the Miner

Press `Ctrl+C` in the terminal window or close the window.

---

## 🔍 How It Works

Scavenger Miner uses the **AshMaize** proof-of-work algorithm, which is:

- **Memory-hard** - Requires significant RAM (ASIC-resistant)
- **CPU-optimized** - Designed for general-purpose processors
- **Fair** - Equal opportunity for standard consumer hardware

**Mining Process:**
1. **Fetch Challenge** - Get a cryptographic puzzle from the network
2. **Initialize ROM** - Set up 1GB of random data based on challenge parameters
3. **Mine Solutions** - Search for nonces that satisfy the difficulty requirement
4. **Submit Solutions** - Send valid solutions to the network
5. **Earn Rewards** - Receive NIGHT tokens proportional to work contributed

---

## 📈 Performance Optimization

### Tips for Best Results

1. **Run on AC Power** (laptops) - Prevents CPU throttling
2. **Ensure Good Cooling** - Keep CPU temps below 80°C
3. **Close Background Apps** - Free up CPU resources

### Monitoring Performance

The miner displays:
- **Hash rate** - Hashes per second (H/s)
- **Total hashes** - Total attempts made
- **Success rate** - Percentage of tasks completed
- **Session statistics** - Tasks, solutions, uptime

---

## 🛠️ Troubleshooting

### Common Issues

**"No tasks available"**
- Normal condition when all tasks are being mined
- Miner automatically retries every 60 seconds
- No action needed

**Miner crashes or stops**
- Check available RAM (need 3GB+ free)
- Verify stable internet connection
- Restart the miner

**High CPU usage**
- Expected! Uses 50% of CPU cores by default
- Close unnecessary programs if system is slow

**Windows SmartScreen warning**
- Click "More info" → "Run anyway"
- This is normal for new executables

**macOS "unidentified developer"**
- Right-click → Open → Click "Open" again
- Or: System Preferences → Security → "Open Anyway"

For more troubleshooting help, see [USER_MANUAL.md](USER_MANUAL.md).

---

## 🔐 Security

### What the Miner Does

- ✅ Connects to official Scavenger Mine API
- ✅ Performs cryptographic hash calculations
- ✅ Submits solutions to earn rewards

### What It Does NOT Do

- ❌ Collect personal information
- ❌ Require private keys or passwords
- ❌ Install software or services


---

## 🙏 Acknowledgments

- **[AshMaize](https://github.com/input-output-hk/ce-ashmaize)** - The ASIC-resistant hash algorithm
- **[Midnight Network](https://midnight.network/)** - The blockchain platform
- **Input Output Global** - For developing the Midnight blockchain

---

## 📞 Support

### Getting Help

- 📖 **Documentation:** [USER_MANUAL.md](USER_MANUAL.md)

### Reporting Issues

When reporting issues, please include:
- Operating system and version
- CPU and RAM specifications
- Full error message (copy exact text)
- Steps to reproduce the issue

---

## 📊 Project Status

- ✅ **Stable** - Ready for production use
- 🔄 **Actively Maintained** - Regular updates and bug fixes
- 📱 **Multi-Platform** - Windows, macOS, Linux

---

## 📸 Screenshots

### Windows
```
C:\ScavengerMiner> scavenger-miner.exe wallets.txt 50
╔════════════════════════════════════════╗
║   Scavenger Mine Miner v4.1            ║
╚════════════════════════════════════════╝
Fetching new task...
✓ Mining started
```

### macOS/Linux
```bash
$ ./scavenger-miner
╔════════════════════════════════════════╗
║   Scavenger Mine Miner v4.1            ║
╚════════════════════════════════════════╝
System: 8 vCPUs, using 4 mining threads
Hash rate: 125.34 H/s
```

---

## 🌟 Star History

If this project helped you, consider giving it a ⭐ on GitHub!

---

## 📝 Changelog

### v1.0.0 (2025-11-XX)
- Initial release
- Multi-threaded mining support
- ROM caching optimization
- Automatic task management
- Cross-platform support (Windows, macOS, Linux)

See [CHANGELOG.md](CHANGELOG.md) for full version history.

---

## 🎯 Key Features Summary

| Feature | Description |
|---------|-------------|
| 🚀 **Zero Installation** | Download and run immediately |
| ⚡ **Multi-Threading** | Uses 50% of CPU cores automatically |
| 🔄 **Auto-Fetch** | Gets tasks from network automatically |
| 📤 **Auto-Submit** | Submits solutions automatically |
| 💾 **ROM Caching** | Reuses memory for efficiency |
| 🖥️ **Cross-Platform** | Windows, macOS (Intel & ARM), Linux |
| 📊 **Real-Time Stats** | Live hash rate and progress |
| 🎛️ **Low Impact** | Uses 50% CPU, computer stays usable |

---

**Ready to start mining? [Download the latest release now!](https://github.com/danny-nguyen-2702/scavenger-miner/releases/latest)**
