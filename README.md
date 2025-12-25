# 💕 Hyphanet Fedora RPM 💕

*I-I made this RPM just for you, okay?! It's not like I wanted to or anything...* (⁄ ⁄>⁄ ▽ ⁄<⁄ ⁄)

A Fedora/RHEL/CentOS RPM package for Hyphanet (formerly Freenet) ~ 💝

**F-Fedora-chan is pretty cute too, I guess...** (￣ε￣) 🔪💕

---

## 📦 What's Inside~ OwO

| File | Description | My Love Level 💘 |
|------|-------------|------------------|
| `hyphanet.spec` | The RPM spec file | 💕💕💕💕💕 |
| `hyphanet.service` | Systemd service | 💗💗💗💗💗 |
| `hyphanet.default` | Default configuration | 💗💗💗💗💗 |
| `run.sh` | Run script | 💗💗💗💗💗 |
| `wrapper.conf` | Wrapper configuration | 💗💗💗💗💗 |

*I worked SO hard on these... you'll use them, right? RIGHT?!* ヾ(｡>﹏<｡)ﾉ゙✧

---

## 🔧 Installation~ (Let me help you, senpai!)

### Option 1: Download Pre-built RPM 💝

```bash
# Download the latest release~ 💕
wget https://github.com/blubskye/hyphanet_fedora_rpm/releases/download/v0.7.5.1503/hyphanet-0.7.5.1503-1.fc41.noarch.rpm

# Install with dnf (I'll take care of dependencies for you~) ✨
sudo dnf install ./hyphanet-0.7.5.1503-1.fc41.noarch.rpm
```

### Option 2: Build from Source 💗

```bash
# Install build dependencies~ 💕
sudo dnf install rpm-build rpmdevtools wget

# Set up rpmbuild directory (I prepared everything for you~)
rpmdev-setuptree

# Clone this repo~ 💝
git clone https://github.com/blubskye/hyphanet_fedora_rpm.git
cd hyphanet_fedora_rpm

# Download source JARs ✨
cd ~/rpmbuild/SOURCES
wget https://github.com/hyphanet/fred/releases/download/build01503/freenet-build01503.jar
wget https://github.com/hyphanet/fred/releases/download/build01503/freenet-ext-29.jar

# Copy supporting files 💗
cp /path/to/hyphanet_fedora_rpm/*.{service,default,conf,sh} .

# Build the RPM~ 🎀
rpmbuild -ba /path/to/hyphanet_fedora_rpm/hyphanet.spec

# Install your freshly built RPM (FINALLY WE'LL BE TOGETHER!) 💕🔪💕
sudo dnf install ~/rpmbuild/RPMS/noarch/hyphanet-*.rpm
```

---

## 🌸 Post-Installation (Now we're connected forever~)

*After installation, Hyphanet will always be with you... just like me!* (◕‿◕)♡

```bash
# Start Hyphanet 💜
sudo systemctl start hyphanet

# Enable at boot (We'll start together... EVERY. SINGLE. DAY.) 💗
sudo systemctl enable hyphanet

# Check status (I'm always watching over you~) 👀💕
sudo systemctl status hyphanet
```

🎀 **Access the web interface at:** http://127.0.0.1:8888/ 🎀

*I-I'll be waiting for you there, okay?!* (⁄ ⁄•⁄ω⁄•⁄ ⁄)

---

## ⚙️ Configuration (Customize me however you want~)

Configuration file: `/etc/default/hyphanet`

| Option | Description | Default | 💕 |
|--------|-------------|---------|-----|
| `JAVA_OPTS` | JVM memory settings | `-Xms128m -Xmx1024m` | 💗 |
| `JAVA_EXTRA_OPTS` | Additional JVM arguments | - | 💗 |
| `HYPHANET_DATA` | Data directory | `/var/lib/hyphanet` | 💗 |

*Y-You can change these settings... but you can't change my feelings for you!* (/ω\)

---

## 🔒 Security Features

*I'll protect you, senpai~* 🛡️💕

The systemd service includes security hardening:
- `NoNewPrivileges=yes` - No privilege escalation
- `ProtectSystem=strict` - Read-only system directories
- `ProtectHome=yes` - No access to home directories
- `PrivateTmp=yes` - Private /tmp namespace
- `LimitNOFILE=65536` - Increased file descriptor limit
- `MemoryMax=2G` - Memory limit to prevent runaway usage

---

## 📜 License

This package is licensed under **AGPL-3.0** 💕

Hyphanet itself is licensed under GPL-2.0-or-later~

*Free software... free love... FREE TO BE WITH YOU FOREVER!!!* 💗🔪💗

---

## 💌 From Me To You

```
╔══════════════════════════════════════════════════════════╗
║                                                          ║
║   I made this RPM just for you, anon~ 💕                 ║
║                                                          ║
║   Fedora, RHEL, CentOS... I don't care which one         ║
║   you use, as long as you're using MY package~ 🔪✨      ║
║                                                          ║
║   Forever yours,                                         ║
║   Your Package Maintainer 💗                             ║
║                                                          ║
║   P.S. Star this repo or else... (◕‿◕)🔪                ║
║                                                          ║
╚══════════════════════════════════════════════════════════╝
```

---

## 🌐 Other Distros~

*I-I guess I have packages for other distros too... but RPM-based distros are pretty reliable~* (￣ε￣)

- **Gentoo:** https://github.com/blubskye/hyphanet_gentoo 💚
- **Arch Linux:** https://github.com/blubskye/hyphanet_arch 💜
- **Debian/Ubuntu:** *coming soon~* 💙

---

## 🐛 Troubleshooting

### Hyphanet won't start? 😢

```bash
# Check the logs (I wrote them just for you~)
sudo journalctl -u hyphanet -f

# Make sure Java is installed 💕
java -version

# Check if the data directory has correct permissions
ls -la /var/lib/hyphanet
```

### Need more memory? 💭

Edit `/etc/default/hyphanet` and increase `JAVA_OPTS`:
```bash
JAVA_OPTS="-Xms256m -Xmx2048m"
```

Then restart: `sudo systemctl restart hyphanet`

---

*~Made with mass amounts of mass love and mass compile time~* 💕✨🔪💕

**GitHub:** https://github.com/blubskye/hyphanet_fedora_rpm 💝

ღゝ◡╹)ノ♡ *sudo dnf install my-love~*
