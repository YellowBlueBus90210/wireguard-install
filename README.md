# WireGuard installation script (Forked Version)

This repository is a fork of [WireGuard Install Script](https://github.com/angristan/wireguard-install) aimed at providing additional features and customizations for specific use cases such as facilitating the deployment of WireGuard across multiple servers by automating server-specific configurations. All credit for the original work goes to the authors of the [original WireGuard Install Script](https://github.com/angristan/wireguard-install).

## Modifications

- **Custom Installation Script to Prompt for Server Name**: Enhances setup efficiency by automatically incorporating server names into configuration file names, thus eliminating manual renaming and reducing setup errors.
- **Output Files Naming Convention**: Configuration files are now named following the `serverName-clientName.conf` convention to streamline identification and management of multiple server configurations.

## Important Notice
This fork has been customized to streamline the setup process for multiple WireGuard servers by automating the inclusion of server names in the configuration file names. Please note that this modification eliminates the interface name from the output file names. As a result, this script is optimized for scenarios where a single WireGuard interface per server is sufficient. If your deployment requires multiple WireGuard interfaces on the same server, with distinct configurations, this version of the script may not support that use case directly.

This change was made to simplify management for users typically deploying a single interface per server but may limit flexibility for more complex setups. If you need to manage multiple interfaces on the same server, additional manual adjustments will be necessary to differentiate the configuration files appropriately.
## Usage
Download and execute the script. Answer the questions asked by the script and it will take care of the rest.

```bash
curl -O https://raw.githubusercontent.com/YellowBlueBus90210/wireguard-install/master/wireguard-install.sh
chmod +x wireguard-install.sh
./wireguard-install.sh
```

This will install WireGuard (kernel module and tools) on the server, configure it, create a systemd service, and generate a client configuration file. To add or remove clients, simply run the script again.

## Acknowledgments

Thank you to the creators and contributors of the [original WireGuard Install Script](https://github.com/angristan/wireguard-install) for their foundational work.

## Contributing

Contributions to this fork are welcome. Please submit a pull request or create an issue for any features or fixes you'd like to propose.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
