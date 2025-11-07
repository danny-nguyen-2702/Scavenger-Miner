# Scavenger-Miner

A high-performance, profit-sharing mining client for the Midnight Network Scavenger Mine program. This miner automatically distributes mining efforts between the operator and users based on a configurable ratio.

## Features

- **Profit Sharing**: Automatically mines solutions for both operator and user wallets based on a ratio (5% for operator)
- **CPU Usage Control**: Adjust CPU usage from 1-100% to match your system's capabilities
- **Multi-Wallet Support**: Mine for multiple user wallets simultaneously
- **Cross-Platform**: Available for Windows, Linux, and macOS
- **Optimized Performance**: Built with Rust for maximum efficiency using the AshMaize algorithm

## System Requirements

### Minimum Requirements
- **CPU**: 2 cores or more
- **RAM**: 2 GB available memory
- **Storage**: 50 MB free disk space
- **Internet**: Stable internet connection

### Recommended Requirements
- **CPU**: 4+ cores
- **RAM**: 4 GB available memory
- **Storage**: 100 MB free disk space

## Installation

### Windows

1. Download the latest `scavenger-miner-windows.exe` from the [Releases](https://github.com/danny-nguyen-2702/Scavenger-Miner/releases) page
2. Create a `wallets.txt` file **in the same directory**
3. Add your Cardano wallet addresses (one per line)
4. Double-click the executable or run from Command Prompt

### Linux

1. Download the latest `scavenger-miner-linux` binary
2. Make it executable:
   ```bash
   chmod +x scavenger-miner-linux
   ```
3. Create a `wallets.txt` file in the same directory
4. Add your Cardano wallet addresses (one per line)
5. Run the miner:
   ```bash
   ./scavenger-miner-linux
   ```

### macOS

1. Download the latest `scavenger-miner-macos` binary
2. Make it executable:
   ```bash
   chmod +x scavenger-miner-macos
   ```
3. Create a `wallets.txt` file in the same directory
4. Add your Cardano wallet addresses (one per line)
5. Run the miner:
   ```bash
   ./scavenger-miner-macos
   ```

**Note**: On macOS, you may need to allow the app in System Preferences > Security & Privacy if you see a security warning.

## Quick Start

1. **Prepare your wallet file** (`wallets.txt`):
   ```
   addr_test1qq4dl3nhr0axurgcrpun9xyp04pd2r2dwu5x7eeam98psv6dhxlde8ucclv2p46hm077ds4vzelf5565fg3ky794uhrq5up0he
   addr_test1qrv3cp0m9u7y0elmk0r9wa6an5vfm24ydp5rlau99jxwvaxvj8fgfutr2sevrpsnkx2t6xgqmvdlz8jth8a5phq2wrdqklv2tz
   ```

2. **Run the miner** with default settings:
   ```bash
   ./scavenger-miner
   ```

3. **Or specify CPU usage** (1-100%):
   ```bash
   ./scavenger-miner 75
   ```

## Configuration

### Wallet Configuration (`wallets.txt`)

Create a text file named `wallets.txt` in the same directory as the miner executable. Add one Cardano wallet address per line:

```
addr_test1qq4dl3nhr0axurgcrpun9xyp04pd2r2dwu5x7eeam98psv6dhxlde8ucclv2p46hm077ds4vzelf5565fg3ky794uhrq5up0he
addr_test1qrv3cp0m9u7y0elmk0r9wa6an5vfm24ydp5rlau99jxwvaxvj8fgfutr2sevrpsnkx2t6xgqmvdlz8jth8a5phq2wrdqklv2tz
```

**Important**: 
- All addresses must be registered with the Scavenger Mine program
- Use Cardano testnet or mainnet addresses depending on the network
- Empty lines and lines starting with `#` will be ignored

### CPU Usage

Control how much of your CPU the miner uses:

```bash
# Use 50% of CPU 
./scavenger-miner

# Use 100% of CPU (maximum performance)
./scavenger-miner wallets.txt 100

# Use 25% of CPU (light mining)
./scavenger-miner wallets.txt 25
```

**Default**: If no value is specified, the miner uses 100% of available CPU cores.

## How It Works

### Profit Sharing Mechanism

The miner operates in cycles, distributing mining effort between:

1. **Operator Wallet**: Solutions submitted to the operator's centralized system
2. **User Wallets**: Solutions submitted directly to the Scavenger Mine API

**Example**: With a 5% (1:19) ratio:
- 1 solution mined for the operator wallet
- 19 solutions mined for user wallets (distributed among all addresses in `wallets.txt`)
- Cycle repeats indefinitely


### Mining Process

1. Miner starts and loads wallet addresses from `wallets.txt`
2. **For Operator Wallet**:
   - Fetches mining task from operator API
   - Finds valid nonce using AshMaize algorithm
   - Submits solution to operator's server
3. **For User Wallets**:
   - Fetches current challenge from Scavenger Mine API
   - Finds valid nonce for each user wallet
   - Submits solutions directly to Scavenger Mine API
4. Repeats from step 2

## Output and Monitoring

The miner provides real-time console output showing:

- Current mining status
- Profit-sharing ratio
- Solutions found and submitted
- CPU usage and performance metrics
- Error messages (if any)

Example output:
```
[INFO] Scavenger Profit Miner v1.0.0
[INFO] CPU Usage: 75%
[INFO] Loaded 2 wallet addresses
[INFO] Profit Sharing Ratio: 1:19
[INFO] Mining cycle started...
[SUCCESS] Solution found for operator wallet (Challenge: **D07C10)
[SUCCESS] Solution found for user wallet (addr_test1qq4dl...)
[INFO] Submitting solutions...
[SUCCESS] All solutions submitted successfully
```

## Troubleshooting

### Common Issues

**"Failed to read wallets.txt"**
- Ensure `wallets.txt` exists in the same directory as the miner
- Check file permissions
- Verify the file contains valid wallet addresses

**"Invalid wallet address"**
- All wallet addresses must be valid Cardano addresses
- Addresses must start with `addr1` (mainnet)
- Remove any extra spaces or characters

**High CPU usage affecting system performance**
- Reduce CPU usage parameter: `./scavenger-miner wallets.txt 50`
- Close other resource-intensive applications
- Ensure adequate cooling for your system

**"Address not registered"**
- Register your wallet addresses with Scavenger Mine before mining
- Visit the Scavenger Mine portal to complete registration

### Performance Optimization

- **CPU Usage**: Start with 50-75% and adjust based on your system
- **Number of Wallets**: Mining with 10-20 wallets provides optimal performance
- **Internet Connection**: Ensure stable, low-latency connection
- **System Resources**: Close unnecessary applications while mining

## Security and Privacy

- **Private Keys**: This miner **NEVER** requires or handles private keys
- **Wallet Addresses**: Only public wallet addresses are used
- **Network Communication**: All API communication uses HTTPS
- **Data Collection**: No personal information is collected

## Important Notes

### Profit Sharing

- The profit-sharing ratio is set by the operator and may change
- Users receive solutions proportional to the ratio and number of wallets
- All solutions are verified on-chain through Scavenger Mine receipts

### Mining Rewards

- NIGHT token allocations are determined by the Scavenger Mine program
- Rewards are proportional to the number of valid solutions submitted
- Solutions submitted to operator wallet are managed by the operator
- Solutions for user wallets are credited directly to those addresses

### Best Practices

1. **Monitor Regularly**: Check console output for errors or issues
2. **Stable Operation**: Keep your computer running during mining
3. **Internet Connection**: Maintain stable internet connectivity
4. **System Cooling**: Ensure adequate cooling, especially at high CPU usage
5. **Backup Wallets**: Keep a backup of your `wallets.txt` file

## Support

For issues, questions, or support:

- **Documentation**: See [USER_MANUAL.md](USER_MANUAL.md) for detailed instructions
- **GitHub Issues**: Report bugs or request features
- **Community**: Join our Discord/Telegram community

## Disclaimer

This software is provided "as is" without warranty of any kind. Mining cryptocurrency involves computational costs (electricity, hardware wear). Users are responsible for:

- Ensuring wallet addresses are correctly registered **before** mining
- Monitoring mining operations
- Understanding the profit-sharing agreement
- Complying with local regulations regarding cryptocurrency

The operator reserves the right to adjust profit-sharing ratios to maintain sustainable operations.

## License

[Insert your chosen license here - e.g., MIT, Apache 2.0, GPL-3.0]

## Acknowledgments

- Built for the [Midnight Network](https://midnight.network/) Scavenger Mine program
- Uses the AshMaize proof-of-work algorithm
- Powered by Rust for maximum performance

---

**Version**: 1.0.0  
**Last Updated**: November 2025  
**Scavenger Mine Phase**: Active (Days 1-21)
