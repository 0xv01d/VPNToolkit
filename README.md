# VPNToolkit

VPNToolkit is a Bash script for managing VPN configurations using OpenVPN. It provides functionalities to start, stop, add, remove, and list VPNs, as well as manage VPN logs and backups. This script requires root or sudo privileges to run properly.

## Features

- **Start VPN**: Activate a VPN configuration.
- **Stop VPN**: Deactivate the active VPN.
- **Add VPN**: Add a new VPN configuration.
- **Remove VPN**: Remove an existing VPN configuration.
- **List VPNs**: List all available VPN configurations.
- **Manage Logs**: Clean, show, and rotate logs.
- **Backup/Restore VPNs**: Backup and restore VPN configurations.
- **Check VPN Status**: Check if a VPN is currently running.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/0xv01d/VPNToolkit.git
    cd VPNToolkit
    ```

2. Make the script executable:
    ```sh
    chmod +x VPNToolkit.sh
    ```

## Usage

Run the script with `sudo` followed by the desired options.

```sh
sudo ./VPNToolkit.sh [OPTIONS]...
```

## Options

   - **-s** : Startup (Create the .vpns directory)
   - **-u** : Up VPN
   - **-d** : Down VPN
   - **-n** : VPN name/pattern
   - **-a** : Add VPN
   - **-r** : Remove VPN
   - **-l** : List VPNs
   - **-h** : Help Panel
   - **-c** : Clean Logs
   - **-f** : Show Log
   - **-k** : Check VPN Status
   - **-o** : Rotate Logs
   - **-b** : Backup VPNs

## Examples

Create .vpns directory:
```sh
sudo ./VPNToolkit.sh -s
```

Turn on VPN:
```sh
sudo ./VPNToolkit.sh -u -n 'vpn_name/vpn_pattern'
```

Turn on VPN with OpenVPN options:
```sh
export VPNARGS='--option1 arg1 --option2 arg2...'
sudo -E ./VPNToolkit.sh -u -n 'vpn_name/vpn_pattern'
```

Turn off VPN:
```sh
sudo ./VPNToolkit.sh -d
```

Add VPN:
```sh
sudo ./VPNToolkit.sh -a 'vpn_path'
```

Remove VPN:
```sh
sudo ./VPNToolkit.sh -r 'vpn_name'
```

List available VPNs:
```sh
sudo ./VPNToolkit.sh -l
```

Clean logs:
```sh
sudo ./VPNToolkit.sh -c
```

Show log:
```sh
sudo ./VPNToolkit.sh -f 'log_name/log_pattern'
```

Check VPN status:
```sh
sudo ./VPNToolkit.sh -k
```

Rotate logs:
```sh
sudo ./VPNToolkit.sh -o
```

Backup VPNs:
```sh
sudo ./VPNToolkit.sh -b
```

Restore VPNs:
```sh
sudo ./VPNToolkit.sh -p 'backup_file'
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contributing

Contributions are welcome, fork this repository and submit a pull request for any improvements.

---

**Author:** 
**0xv01d**
[Website](https://0xv01d.github.io)
