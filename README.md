# 🖥️ Script View
<img src="https://raw.githubusercontent.com/kangetzyyrupis/rdpinstall/main/.bener/imgbener.jpg" alt="Girl in a jacket" width="420" height="120">

# 🚀💾 Auto Install Windows Docker
```bash
bash <(curl -fsSL https://raw.githubusercontent.com/kangetzyyrupis/rdpinstall/main/autoinstall)
```

# ⚙️ Manual instalasi

```bash
sudo apt update
sudo apt install snapd -y
```
# 🚢 Install Docker snapd
```bash
sudo snap install docker
```
# 🔧 Configurasi Windows
#Create compose.yml file

```bash
nano compose.yml
```
#Copy paste the code below into compose.yml

```bash
services:
  windows:
    image: dockurr/windows
    container_name: windows
    environment:
      VERSION: 11
      REGION: en-US
      KEYBOARD: en-US
      USERNAME: YOUR_USERNAME
      PASSWORD: YOUR_PASSWORD
      RAM_SIZE: 4G
      CPU_CORES: 4
      DISK_SIZE: 70G
    devices:
      - /dev/kvm
    cap_add:
      - NET_ADMIN
    ports:
      - 8006:8006
      - 3389:3389/tcp
      - 3389:3389/udp
    restart: no
```

#Note

-Replace "YOUR_USERNAME" with whatever you want.

-Replace "YOUR_PASSWORD" with whatever you want.

#Save with CTRL X+Y ENTER

# 🚀 Run Windows on docker
```bash
docker compose up -d
```
#Note :
-You are not using Docker snap so maybe the command is not the same.

#Check installation via browser: http://yourip:8006

#Login Remote desktop with your username and password with port 3389.

## 🙏 Credit
Big thanks to [dockur/windows](https://github.com/dockur/windows) for their amazing work! 🚀
