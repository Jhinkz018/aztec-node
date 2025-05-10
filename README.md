# Aztec Sequencer Setup - Alpha Testnet

This repository contains an automated script for setting up and running an Aztec Sequencer node on the Alpha Testnet. The script streamlines the installation process, making it accessible for both newcomers and experienced blockchain developers.

## Overview

The `aztec.sh` script automates the installation and configuration of an Aztec Sequencer node on the Alpha Testnet. It handles the following tasks:

- Installing Docker and Docker Compose (if not already installed)
- Installing Node.js (if not already installed)
- Installing the Aztec CLI
- Setting up the Aztec Alpha Testnet environment
- Configuring your node with the necessary RPC URLs and validator private key
- Starting your Aztec Sequencer node

## Requirements

- Ubuntu/Debian-based Linux OS
- Root or sudo privileges
- Internet connection
- L1 Execution Client (EL) RPC URL
- L1 Consensus Client (CL) RPC URL
- Validator Private Key
- Blob Sink URL (optional)

## Quick Start

1. Clone this repository:
   ```bash
   git clone https://github.com/airdropinsiders/Aztec-Node.git
   cd Aztec-Node
   ```

2. Make the script executable:
   ```bash
   chmod +x aztec.sh
   ```

3. Run the script with sudo:
   ```bash
   sudo ./aztec.sh
   ```

4. Follow the prompts to provide the required RPC URLs and validator private key.

## Tutorial: Obtaining RPC URLs

### L1 Execution Client (EL) RPC URL

This URL is used to connect to an Ethereum execution client on the Sepolia testnet.

1. Sign up or log in at [Alchemy](https://dashboard.alchemy.com/)
2. Create a new app:
   - Click "Create App"
   - Select "Ethereum" as the chain
   - Select "Sepolia" as the network
   - Give your app a name (e.g., "Aztec Sequencer")
   - Click "Create App"
3. Once your app is created, click on "View Key"
4. Copy the HTTPS URL, which should look like:
   ```
   https://eth-sepolia.g.alchemy.com/v2/YOUR_API_KEY
   ```

### L1 Consensus Client (CL) RPC URL

This URL is used to connect to an Ethereum consensus client on the Sepolia testnet.

1. Sign up or log in at [DRPC](https://drpc.org/)
2. Create an API key:
   - Go to the "API Keys" section
   - Click "Create API Key"
   - Give your key a name (e.g., "Aztec Sequencer")
   - Select "Sepolia" network
3. Once your key is created, copy the HTTPS URL, which should look like:
   ```
   https://lb.drpc.org/ogrpc?network=sepolia&dkey=YOUR_API_KEY
   ```

### Alternative RPC Providers

You can also use other RPC providers such as:

- [Infura](https://infura.io/)
- [QuickNode](https://www.quicknode.com/)
- [Ankr](https://www.ankr.com/)
- [Chainstack](https://chainstack.com/)

Follow a similar process on these platforms to obtain your RPC URLs for the Sepolia testnet.

## Checking Node Status

After installation, you can check the status of your node:

```bash
docker-compose logs -f
```

Your node data is stored in the `data` directory created in the same location as the script.

## Troubleshooting

If you encounter issues:

1. Check your Docker installation:
   ```bash
   docker --version
   docker-compose --version
   ```

2. Verify your RPC URLs are correct and working.

3. Ensure your server has enough resources:
   - At least 8 CPU cores
   - 16GB RAM
   - 100GB free disk space
   - 25 Mbps upload

4. Check firewall settings to ensure the required ports are open.

## Additional Resources

- [Aztec Documentation](https://docs.aztec.network/)
- [Aztec Discord](https://discord.gg/aztec)
- [Aztec Forum](https://forum.aztec.network/)

## Version Information

- Script version: v0.85.0-alpha-testnet.5
- Compatible with Aztec Protocol version: 0.85.0-alpha-testnet.5

## Disclaimer

This is an Alpha Testnet setup. It's not meant for production use and may have bugs or issues. Use at your own risk.

## License

[MIT License](LICENSE)
