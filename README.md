# ccminer_versus-nicehash
Mine VerusHash on Android devices using ccminer and get paid in Bitcoin (BTC) through NiceHash! This repository provides a complete guide to setting up and optimizing VerusHash mining on rooted Android phones or custom ROMs, allowing you to mine efficiently and earn BTC.

# ccminer_verushash_nicehash
Mine VerusHash on Android using **ccminer** and get paid in Bitcoin (BTC) via NiceHash! This repository provides a step-by-step guide to set up and configure ccminer on rooted Android devices or custom ROMs, allowing you to optimize mobile mining and earn BTC with minimal resource consumption.

# VerusHash Mining on Android with ccminer via NiceHash

This repository provides instructions to mine VerusHash on Android devices using **ccminer** and get paid in Bitcoin through **NiceHash**. Follow the steps below to set up your mobile mining rig.

## Prerequisites

- **Linux Knowledge**: Some fundamental Linux knowledge is required. Brush up on it via an online course if needed.
- **Linux Screen**: Learn how to use `screen` for long-term mining sessions.
- **SSH and SCP**: Recommended for remote management.
- **Stable Network**: Ensure a stable WiFi or cellular connection.

## Installation Instructions

1. **Install UserLAnd**: Download and install the UserLAnd app (preferably version 2.8.3 from the app store or APK).
2. **Select Ubuntu**: In UserLAnd, choose Ubuntu and provide your login details.
3. **Choose SSH**: Select the SSH option and wait for Ubuntu to install.
4. **Log In**: Once installed, log in to your Ubuntu account.
5. **Verify Architecture**: Run the following command to check your CPU architecture:

    ```
    lscpu
    ```

- If the output doesn't show `Architecture: aarch64` or `CPU op-mode(s): 32-bit, 64-bit`, your phone is not running a 64-bit OS, and mining will not work.

6. **Install Mining Script**:

    ```
    curl -o- -k https://raw.githubusercontent.com/tanishdt/ccminer/main/install.sh | bash
    ```

7. **Configure Mining Settings**:
- Open `config.json`:
    ```
    nano config.json
    ```
- Adjust the NiceHash pool, BTC payout address (from your NiceHash wallet), and worker name.
- in the config file, algorithm name for verus is wrong, correct name: verus
- Save and exit by pressing `<CTRL>-X`, then `Y` and `<ENTER>`.

8. **Start Mining**:
- Start the miner with:
    ```
    ~/ccminer/start.sh
    ```

***Inspiration taken from https://github.com/TheRetroMike/VerusCliMining***
