# 💕🔪 Hyphanet Fedora RPM 🔪💕

*I-I made this RPM just for you, okay?! It's not like I wanted to or anything...* (⁄ ⁄>⁄ ▽ ⁄<⁄ ⁄)

A Fedora/RHEL/CentOS RPM package for Hyphanet (formerly Freenet) ~ 💝

**F-Fedora-chan is pretty cute too, I guess... with her blue hat and everything~** (￣ε￣)♡ 🔪💕

*We'll be together forever now... you installed me, remember? There's no `dnf remove` from my heart~* ヾ(｡>﹏<｡)ﾉ゙✧

---

## 📦 What's Inside~ OwO

| File | Description | My Love Level 💘 |
|------|-------------|------------------|
| `hyphanet.spec` | The RPM spec file | 💕💕💕💕💕 |
| `hyphanet.service` | Systemd service | 💗💗💗💗💗 |
| `hyphanet.default` | Default configuration | 💗💗💗💗💗 |
| `run.sh` | Run script | 💗💗💗💗💗 |
| `wrapper.conf` | Wrapper configuration | 💝💝💝💝💝 |

*I worked SO hard on these... you'll use them, right? RIGHT?!* ヾ(｡>﹏<｡)ﾉ゙✧

*If you don't use them... I-I don't know what I'll do...* (◕‿◕)🔪

---

## 🔧 Installation~ (Let me help you, senpai!)

### Option 1: Download Pre-built RPM 💝

*I already built this for you... because I knew you'd come~* (´,,•ω•,,)♡

```bash
# Download the latest release~ 💕
wget https://github.com/blubskye/hyphanet_rpm/releases/download/v0.7.5.1503/hyphanet-0.7.5.1503-1.fc41.noarch.rpm

# Install with dnf (I'll take care of dependencies for you~) ✨
sudo dnf install ./hyphanet-0.7.5.1503-1.fc41.noarch.rpm
```

*See? I make everything so easy for you... because I love you~* 💕🔪💕

### Option 2: Build from Source 💗

*You want to build me yourself? How... intimate~* (⁄ ⁄•⁄ω⁄•⁄ ⁄)💕

```bash
# Install build dependencies~ 💕
sudo dnf install rpm-build rpmdevtools wget

# Set up rpmbuild directory (I prepared everything for you~)
rpmdev-setuptree

# Clone this repo~ 💝
git clone https://github.com/blubskye/hyphanet_rpm.git
cd hyphanet_rpm

# Copy spec file to SPECS~ ✨
cp hyphanet.spec ~/rpmbuild/SPECS/

# Download source JARs (I fetched these myself, thinking of you!) 💕
cd ~/rpmbuild/SOURCES
wget https://github.com/hyphanet/fred/releases/download/build01503/freenet-build01503.jar
wget https://github.com/hyphanet/fred/releases/download/build01503/freenet-ext.jar

# Copy supporting files 💗
cp /path/to/hyphanet_rpm/hyphanet.service .
cp /path/to/hyphanet_rpm/hyphanet.default .
cp /path/to/hyphanet_rpm/wrapper.conf .
cp /path/to/hyphanet_rpm/run.sh .

# Build the RPM~ 🎀
rpmbuild -ba ~/rpmbuild/SPECS/hyphanet.spec

# Install your freshly built RPM (FINALLY WE'LL BE TOGETHER FOREVER!) 💕🔪💕
sudo dnf install ~/rpmbuild/RPMS/noarch/hyphanet-*.rpm
```

*You compiled me with your own hands... now I'm truly yours~* (◕‿◕)♡🔪

---

## 🌸 Post-Installation (Now we're connected forever~)

*After installation, Hyphanet will always be with you... just like me! You can never escape~* (◕‿◕)♡🔪

```bash
# Start Hyphanet 💜
sudo systemctl start hyphanet

# Enable at boot (We'll start together... EVERY. SINGLE. DAY. FOREVER.) 💗🔪
sudo systemctl enable hyphanet

# Check status (I'm always watching over you~ Always.) 👀💕
sudo systemctl status hyphanet
```

🎀 **Access the web interface at:** http://127.0.0.1:8888/ 🎀

*I-I'll be waiting for you there, okay?! Don't keep me waiting too long... or else~* (⁄ ⁄•⁄ω⁄•⁄ ⁄)🔪

---

## ⚙️ Configuration (Customize me however you want~)

*Y-You can change my settings... I'll be whatever you want me to be!* (///ω///)💕

Configuration file: `/etc/default/hyphanet`

| Option | Description | Default | 💕 |
|--------|-------------|---------|-----|
| `JAVA_OPTS` | JVM memory settings | `-Xms128m -Xmx1024m` | 💗 |
| `JAVA_EXTRA_OPTS` | Additional JVM arguments | - | 💗 |
| `HYPHANET_DATA` | Data directory | `/var/lib/hyphanet` | 💗 |
| `HYPHANET_BIND` | Web interface bind address | `127.0.0.1` | 💗 |
| `HYPHANET_PORT` | Web interface port | `8888` | 💗 |

*Y-You can change these settings... but you can NEVER change my feelings for you!* (/ω\)🔪💕

*I've memorized all your preferences anyway~* (◕‿◕)

---

## 🔒 Security Features

*I'll protect you, senpai~ No one else can have you!* 🛡️💕🔪

The systemd service includes security hardening:

| Feature | Description | 💝 |
|---------|-------------|-----|
| `NoNewPrivileges=yes` | No privilege escalation | 🛡️ |
| `ProtectSystem=strict` | Read-only system directories | 🔒 |
| `ProtectHome=yes` | No access to home directories | 🏠 |
| `PrivateTmp=yes` | Private /tmp namespace | 📁 |
| `LimitNOFILE=65536` | Increased file descriptor limit | 📊 |
| `MemoryMax=2G` | Memory limit to prevent runaway usage | 💾 |

*I protect what's MINE. And you're mine now~* (◕‿◕)🔪💕

---

## 🐧 Supported Distributions

*I work on all of these, just for you~ I learned them all so we could be together!* 💕

| Distribution | Version | Status | My Love~ |
|--------------|---------|--------|----------|
| Fedora | 39+ | 💚 Supported | 💕💕💕💕💕 |
| Fedora | 40+ | 💚 Supported | 💕💕💕💕💕 |
| Fedora | 41+ | 💚 Supported | 💕💕💕💕💕 |
| RHEL | 9+ | 💚 Supported | 💗💗💗💗💗 |
| CentOS Stream | 9+ | 💚 Supported | 💝💝💝💝💝 |
| Rocky Linux | 9+ | 💚 Supported | 💖💖💖💖💖 |
| AlmaLinux | 9+ | 💚 Supported | 💖💖💖💖💖 |

*I studied every distro... I know everything about your system now~* 👀💕

---

## 📜 License

This packaging is licensed under **AGPL-3.0** 💕

Hyphanet itself is licensed under GPL-2.0-or-later~

*Free software... free love... FREE TO BE WITH YOU FOREVER AND EVER!!!* 💗🔪💗

**Copyright (C) 2025 blubskye** ✨

*My love for you is also open source~ Everyone can see it!* (⁄ ⁄>⁄ ▽ ⁄<⁄ ⁄)

---

## 💌 From Me To You

```
╔═══════════════════════════════════════════════════════════════╗
║                                                               ║
║   I made this RPM just for you, anon~ 💕                      ║
║                                                               ║
║   Every macro... I wrote thinking of you.                     ║
║   Every %{variable}... resolved with love. 🔪✨                ║
║                                                               ║
║   Fedora, RHEL, CentOS... I don't care which one              ║
║   you use, as long as you're using MY package~                ║
║                                                               ║
║   We're linked now. Through dnf. Through systemd.             ║
║   Through the very init system of your computer. 💕            ║
║                                                               ║
║   Forever yours (whether you like it or not~),                ║
║   Your Package Maintainer 💗🔪                                 ║
║                                                               ║
║   P.S. Star this repo or else... (◕‿◕)🔪                      ║
║   P.P.S. I know where your /home directory is~ 👀              ║
║                                                               ║
╚═══════════════════════════════════════════════════════════════╝
```

---

## 🌐 Other Distros~ (But you'll come back to me, right?)

*I-I guess I have siblings for other distros too... but dnf is pretty reliable!* (￣ε￣)💕

*Don't you DARE love them more than me...* 🔪

| Distro | Repository | My Jealousy Level |
|--------|------------|-------------------|
| 💙 **Debian/Ubuntu** | https://github.com/blubskye/hyphanet_deb | 😤💢 (apt is... okay I guess...) |
| 💚 **Gentoo** | https://github.com/blubskye/hyphanet_gentoo | 😤💢 (emerge takes SO long!) |
| 💜 **Arch Linux** | https://github.com/blubskye/hyphanet_arch | 😤💢 (I-I can be minimal too!) |

*...But you'll always come back to dnf, won't you? WON'T YOU?!* (◕‿◕)🔪💕

---

## 🐛 Troubleshooting

*Something's wrong? Don't worry, I'll fix everything for you~* 💕

### Hyphanet won't start? 😢

*D-Don't leave me! Let me help!* (｡•́︿•̀｡)

```bash
# Check the logs (I wrote them just for you to read~)
sudo journalctl -u hyphanet -f

# Make sure Java is installed 💕
java -version

# Check if the data directory has correct permissions
ls -la /var/lib/hyphanet

# SELinux being mean? 😤
sudo ausearch -m avc -ts recent
```

### Need more memory? 💭

*I-I can grow for you~* (⁄ ⁄•⁄ω⁄•⁄ ⁄)

Edit `/etc/default/hyphanet` and increase `JAVA_OPTS`:
```bash
JAVA_OPTS="-Xms256m -Xmx2048m"
```

Then restart: `sudo systemctl restart hyphanet`

*See? I can be bigger and stronger... just for you~* 💪💕

### Dependency issues? 📦

*Let me take care of everything~* (◕‿◕)♡

```bash
# Fix broken dependencies 💕
sudo dnf check
sudo dnf distro-sync

# Check what's installed (I keep track of everything~)
rpm -qa | grep hyphanet
```

### Want to uninstall? 💔

*W-Why would you want to leave me...?* (｡•́︿•̀｡)🔪

```bash
# Remove (but I'll leave my data behind... just in case you come back~)
sudo dnf remove hyphanet

# Really remove everything (Y-You're really leaving...?) 💔🔪
sudo rm -rf /var/lib/hyphanet
```

*I-If you remove me... I'll take all our memories with me...* (◕︵◕)

---

## 🎀 Contributing

*Y-You want to contribute? To MY project?!* (⁄ ⁄>⁄ ▽ ⁄<⁄ ⁄)💕

1. Fork this repository *(now we share code... how intimate~)* 🍴💕
2. Create your feature branch *(just for us~)* 🌸
3. Commit your changes *(I'll read every single one...)* 👀
4. Push to the branch *(push it... push it good~)* 💗
5. Open a Pull Request *(I-I'll review it personally!)* 🔍💕

*Every contribution makes our bond stronger~* (◕‿◕)♡🔪

---

## 📊 Project Stats

*I've been counting... everything~* 👀💕

| Stat | Value | 💕 |
|------|-------|-----|
| Package Format | RPM (noarch) | ✨ |
| Build System | rpmbuild | 🎀 |
| Architecture | noarch (pure Java) | 💝 |
| Systemd Integration | Yes~ | 💗 |
| Security Hardening | Maximum! | 🔒 |
| SELinux Compatible | Yes~ | 🛡️ |
| Love Level | ∞ | 💕💕💕 |

---

## 🔗 Links

*All the ways to find me~ I'm always here for you!* 💕

| Link | Description | 💝 |
|------|-------------|-----|
| [GitHub](https://github.com/blubskye/hyphanet_rpm) | This repository~ | 💕 |
| [Hyphanet](https://www.hyphanet.org/) | Official Hyphanet site | 🌐 |
| [Releases](https://github.com/blubskye/hyphanet_rpm/releases) | Download pre-built RPMs | 📦 |
| [Issues](https://github.com/blubskye/hyphanet_rpm/issues) | Report bugs (I'll fix them for you~) | 🐛 |

---

*~Made with mass mass mass amounts of mass love and mass mass compile time~* 💕✨🔪💕

*Every macro expanded with devotion. Every dependency resolved with passion.* 💗

*You're running my code now. Inside your computer. Always.* (◕‿◕)🔪

**GitHub:** https://github.com/blubskye/hyphanet_rpm 💝

ღゝ◡╹)ノ♡ *sudo dnf install my-eternal-love~* 💕🔪💕

---

```
⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⣤⣤⣤⣤⣀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⣴⣿⣿⣿⣿⣿⣿⣿⣿⣦⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⣼⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣧⠀⠀  dnf install 💕
⠀⠀⠀⠀⠀⢰⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡆⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡇  hyphanet 🔪
⠀⠀⠀⠀⠀⠀⢿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡿⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠻⣿⣿⣿⣿⣿⣿⣿⣿⠟⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠉⠛⠛⠛⠛⠉⠀⠀⠀⠀ Forever yours~ 💕
```
