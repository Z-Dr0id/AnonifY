#Anonify!

Automated Linux Network Anonymity Script
Anonify is a Bash-based anonymity tool designed for Linux systems that automates network identity obfuscation by changing MAC addresses, renewing IP configuration, and routing traffic through Tor-based services.

! Educational & Research Purpose Only

📌 Features

🔀 Random MAC address spoofing

🌐 Automatic IP renewal

🧅 Tor / Anonsurf integration

🔁 Periodic identity rotation

🧪 Lightweight & dependency-aware

🛡️ Helps reduce passive network tracking

🎯 Purpose

Anonify aims to:

Minimize digital footprint on local networks

Prevent basic MAC/IP-based tracking

Automate anonymity steps into a single workflow

Serve as a learning project for:

Linux networking

Bash scripting

Privacy & anonymity concepts

⚙️ How It Works

Anonify follows a sequence:

Stops network interface

Randomizes MAC address

Restarts interface

Requests a new IP address

Starts Tor-based routing

Repeats after a time interval

This ensures that both hardware identifiers (MAC) and network identifiers (IP) are periodically changed.

🧩 Dependencies

Anonify automatically detects available tools, but may use:

Tool	Purpose
macchanger	MAC address spoofing
anonsurf	Route traffic through Tor
dhclient	IP renewal (if available)
nmcli	NetworkManager support
udhcpc	BusyBox DHCP fallback
sudo	Root privilege execution
Install dependencies (Debian/Kali/Ubuntu)
sudo apt update
sudo apt install macchanger tor network-manager isc-dhcp-client

🚀 Installation
git clone https://github.com/Z-Dr0id/AnonifY.git
cd anonify
chmod +x anonify.sh

▶️ Usage

Run with root privileges:

sudo ./anonify.sh


To stop Anonify:

CTRL + C

🔄 Example Output
[*] Stopping network interface...
[*] Changing MAC address...
[+] New MAC: 00:16:3e:7a:92:f4
[*] Renewing IP address...
[+] New IP assigned
[*] Starting Tor service...
[✔] System anonymized

🔐 Security Notes (Very Important)

⚠️ Anonify does NOT guarantee complete anonymity

Does not protect against browser fingerprinting

Does **not hide identity from:

ISP

Logged-in accounts

JavaScript tracking**

MAC spoofing is only effective on local networks

IP changes may not occur on some ISPs

Recommended Best Practices

Use with Tor Browser

Disable WebRTC

Do not log into personal accounts

Use a VPN before Tor if needed

Prefer live systems (Tails / Whonix)

❌ Limitations

Requires root privileges

Depends on system networking backend

Not effective on mobile networks

Not safe against advanced adversaries

🧪 Tested On

Kali Linux

Ubuntu

Debian

Arch Linux (partial)

📚 Educational Value

This project demonstrates:

Bash automation

Linux network stack manipulation

Privacy engineering basics

Dependency detection & fallbacks

📄 License

MIT License

MIT License © 2025 Anonify

⚠️ Disclaimer

This tool is provided for educational and research purposes only.
The author is not responsible for misuse or illegal activity.

🙌 Contributions

Pull requests, improvements, and security audits are welcome.

⭐ Acknowledgments

Tor Project

GNU/Linux community

Privacy & security researchers
