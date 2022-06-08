# dropcheck

For Interop Tokyo 2022


## Requirements

- Ubuntu 22.04
- wget
- mtr

## :warning: Caveats :warning:
Configure DNS addresses 

```sh
DNS_V4=$GOOGLE_PUBLIC_DNS_V4
DNS_V6=$GOOGLE_PUBLIC_DNS_V6
```

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

# Run tests
sudo ./dropcheck en0
```
