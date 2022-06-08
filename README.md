# dropcheck

For Interop Tokyo 2022


## Requirements

- Ubuntu 22.04
- wget
- mtr

## Usage

```sh
# Download this script and make executable
wget https://raw.githubusercontent.com/naoki9911/dropcheck/master/dropcheck
chmod +x dropcheck

# Check the target interface (e.g. en0)
ip link | grep 'UP'

# Turn off interfaces except for the target interface
ip link set en1 down
ip link set en2 down
...

# Run tests with Google DNS config
sudo ./dropcheck en0

# Run tests with DNS config
sudo DNS_V4=1.1.1.1 DNS_V6=2606:4700:4700::1111 ./dropcheck en0
```
