The TIK mainnet genesis is happening on June 10, 2024, at 00:00:00  (UTC). 




Tik died. $TIME Reborn! Its Time To Mine $Time!



[Telegram](https://t.me/+xIQLofb3wKQ2YjM1)
[Web mine](https://timemine.life)



$TIME epoch Genesis timestamp:1728450000





# TIME-CLI : TIME Command-line Interface Tool

TIME-cli is a simple command line tool that you can use to mine, check rewards and claim TIME.

# build TIME cli


   After decompressing the archive, you will get a file named tik.exe. Open the Windows command line tool. Navigate to the current directory, for example.

         cd c:\time_windows
    

   After decompressing the archive, you will get a file named TIME.


# Creat a keypair

Windows:

      time.exe gen
       
Linux:

      ./time gen

- Please note that the keypair in the current directory will look like this:  0xeacafedc18e18848570431fa8ba41ac28bfbca427cb323c105dee4dc32ca13c9.key
- Please deposit at least 1 SUI to start the mining.


# Start mining

Windows:

      time.exe --keypair <KEYPAIR_FILEPATH> mine

Linux:

      ./time --keypair <KEYPAIR_FILEPATH> mine

Use the --lock parameter to lock rewards and increase your share. Eg.

      ./time --keypair <KEYPAIR_FILEPATH> mine --lock 8 

Your share has increased from 10 to 18, and You can only claim your rewards after 8 days. 

# Check rewards

Windows:

       time.exe --keypair <KEYPAIR_FILEPATH> rewards

Linux:

       ./time --keypair <KEYPAIR_FILEPATH> rewards

# Claim TIME to your wallet 

Windows:

       time.exe --keypair <KEYPAIR_FILEPATH> claim

Linux:

       ./time --keypair <KEYPAIR_FILEPATH> claim

# Show the suiprivate key from a keypair

Windows:

       time.exe --keypair <KEYPAIR_FILEPATH> prikey

Linux:

       ./time --keypair <KEYPAIR_FILEPATH> prikey


# Import your suiprivate key to create a keypair

Windows:

       time.exe Import <suiprivate string> 

Linux:

       ./time Import <suiprivate string>


# Usage
time [OPTIONS] --keypair <KEYPAIR_FILEPATH> <COMMAND>

Commands:

       mine     Start mining.
       rewards  Check how much TIME you've earned.
       claim    Claim rewards to your wallet.
       gen      Generate a keypair.
       prikey   Show the suiprivate key from a keypair.
       import   Import your suiprivate key to create a keypair.
       help     Print this message or the help of the given subcommand(s)


Options:

       --rpc <NETWORK_URL>           Network address of your RPC provider default: https://fullnode.testnet.sui.io:443
       --keypair <KEYPAIR_FILEPATH>  Filepath for the keypair to use
       --testnet                     For testnet
       -h, --help                   Print help
       -V, --version                Print version


# Build

- Install RUST. 

Windows: Check this out -->  <a href="https://www.rust-lang.org/tools/install" target="_blank">https://www.rust-lang.org/tools/install</a>

Linux:


      sudo apt update
      sudo apt install build-essential -y
      curl https://sh.rustup.rs -sSf | sh
      . "$HOME/.cargo/env"



- build
         
       git clone https://github.com/GunadhyaMahanta/TimeMine_sui_cli
       cd TIME-cli
       cargo build --release
