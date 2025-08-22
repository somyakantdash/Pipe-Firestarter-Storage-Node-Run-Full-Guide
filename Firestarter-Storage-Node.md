# Firestarter Storage Node Run Full Guide (PC Only)

### Offical Docs by Pipe Network - https://docs.pipe.network/pipe-firestarter-storage

----

## 🧰 Prerequisites
	
### Nothing

----

1️⃣ Dependencies for WINDOWS & LINUX & VPS
```
sudo apt-get update && sudo apt-get upgrade -y
```
```
sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
```
```
sudo apt install -y libssl-dev ca-certificates
```

2️⃣ Install Rustup
```
curl https://sh.rustup.rs -sSf | sh
```
```
source $HOME/.cargo/env
```
```
rustc --version
```

3️⃣ Download Some Files
```
git clone https://github.com/PipeNetwork/pipe.git
cd pipe
```

4️⃣ Install pipe-cli
```
cargo install --path .
```

5️⃣ Verify The Installation
```
pipe -h
```

6️⃣ SetUp Your Account
```
pipe new-user <your_username>
```

- Replace <your_username> with your Name
- Must Save `Solana Pubkey`

7️⃣ Set-Up Your Password
```
pipe set-password
```

8️⃣ Save the File
```
nano ~/.pipe-cli.json
```

9️⃣ Put the Refer Code
```
pipe referral apply SOMYAKAN-TQDP
```

1️⃣0️⃣ Generate Your Referral
```
pipe referral generate
```

1️⃣1️⃣ Check ur Referral Stats
```
pipe referral show
```

1️⃣2️⃣ Swap Sol (Devnet) to Pipe Network

* Solana Devnet Faucet: [HERE](https://faucet.solana.com/)

```
pipe  swap-sol-for-pipe <AMOUNT_SOL>
```

- Swap minimum 1 SOL to pipe

---
---

1️⃣3️⃣ Upload a File

```
pipe upload-file ~/<FILE_PATH> <FILE_NAME>
```

* Replace <FILE_PATH> & <FILE_NAME> with their actual name & path
* Dont upload any `confidential` file (Wallet keys & personal docs)
* You can upload any videos or large file too

### How t Get File Path in ur Local PC

To Enter Ur WSL or Ubuntu Folder
```
explorer.exe .
```
Check ur File Name & Path
```
ls -a
```

1️⃣4️⃣ Create Public Link
```
pipe create-public-link <FILE_NAME>
```

* >Replace <FILE_NAME> which you have used earlier while uploading a file:

1️⃣5️⃣ Check Token-Usage
```
pipe token-usage
```

U can get to know about the usage of the pipe devnet tokens, after uploading and Downloading Files

## 🔶For Next Day Run This Command

#1 Open WSL and Put this Command 
```
cd pipe
```
- Follow 1️⃣2️⃣ Number Point
```
pipe  swap-sol-for-pipe <AMOUNT_SOL>
```
- Follow 1️⃣3️⃣ Number Point
```
pipe upload-file ~/<FILE_PATH> <FILE_NAME>
```
- Follow 1️⃣4️⃣ Number Point
```
pipe create-public-link <FILE_NAME>
```

## Delete Pipe Firestarter Storage Node
```
cargo uninstall pipe
```
```
rm -rf ~/pipe
rm -f ~/.pipe-cli.json
rm -rf ~/.config/pipe
rm -rf ~/.local/share/pipe
```
