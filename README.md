```
# Connect to WLAN (if not LAN)
iwctl --passphrase [password] station wlan0 connect [network]

# Check internet connection
ping -c4 www.archlinux.org

# Check partitions
lsblk

# Create partitions
gdisk /dev/sda
# Partition 1: +512M ef00 (for EFI)
# Partition 2: Available space 8300 (for Linux filesystem)
# (Optional Partition 3 for Virtual Machines)
# Write w, Confirm Y

# Sync package
pacman -Syy

# Install git
pacman -S git

# Clone Installation
git clone https://www.github.com/gbouline/arch-install.git
cd arch-install

# Start the script
./1-install.sh

```
