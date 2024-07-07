# Sonaric AI Node Guide

![image](https://pbs.twimg.com/media/GO0Ojjga4AAqFnm?format=jpg&name=4096x4096)

Minimum System Requirements:
- 4 GB RAM
- 2 CPU cores
- 20 GB free disk space
- 64-bit operating system

### Links
[Explorer](https://tracker.sonaric.xyz/)   /
[Twitter](https://x.com/Sonaricnetwork)    /
[Discord](https://discord.gg/MZ247hw47z) 

## Ports Used:
![image](https://github.com/pvsairam/Sonaric-Network/assets/9134015/f9233407-ed55-4af5-aa18-4656da8e9a39)


## Let's Update the System
```bash
sudo apt update && \
sudo apt install curl git jq build-essential gcc unzip wget lz4 -y
```

## Download the Necessary File and Give Permissions
```bash
wget https://raw.githubusercontent.com/aksamlan/Sonaric/main/sonaric.sh && chmod +x sonaric.sh && ./sonaric.sh
```

## After Installation, Open the Ports
```bash
ufw allow 22
ufw allow ssh
```

## Check if Your Node is Successfully Set Up
```bash
sonaric node-info
```

## Run the GUI

#### Open your local terminal (CMD)
#### Replace "user@your-vps-ip" with your own IP (e.g., root@123.456.789)

```bash
ssh -L 127.0.0.1:44003:127.0.0.1:44003 -L 127.0.0.1:44004:127.0.0.1:44004 -L 127.0.0.1:44005:127.0.0.1:44005 -L 127.0.0.1:44006:127.0.0.1:44006 user@your-vps-ip
```
#### After entering, input your server password to proceed.


### Open link: http://localhost:44004/
#### (Open on the same device where you executed the previous command)
#### Click ⚙ icon, then export json file & save it on the safe place.!!

## Backup Your Information on the Server

```bash
sonaric identity-export -o mysonaric.identity
```

## Now Open the Local terminal(CMD) & Download the JSon file!

```bash
pscp user@your-vps-ip:/path/to/remote/file C:\path\to\local\directory
```

#### Save the mysonaric.identity file in a secure place. It is located in the root directory.

> #### Example:
>
> ```bash
> pscp root@123.456.789:/root/mysonaric.identity C:\Users\Airdrop_OG\Downloads\Sonaric_Keys_Backup
> ```

## To update Sonaric to the latest version, simply use the package manager to update the Sonaric package. [optional]

```bash
apt update
apt upgrade sonaric
```

## To View Your Points on the Server, Enter This Code

```bash
sonaric points
```

## To Change the Name, Enter This Code and Then Write Your New Name

```bash
sonaric node-rename
```

## Leaderboard

> #### Open link: https://tracker.sonaric.xyz/
>
> #### Look up the name of the node that each node will have, and then check your score there. By the way, you can view your points using this link: http://localhost:44004/

### That's a wrap!
