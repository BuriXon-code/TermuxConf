# TermuxConf

## About

**TermuxConf** is a lightweight, browser-based configuration editor for Termux. It helps you manage `~/.termux/termux.properties` without having to edit the file manually.

Use the graphical interface to adjust supported terminal settings, configure hardware keyboard shortcuts, customize the Extra Keys panel, and create or restore configuration backups. TermuxConf is designed to run directly in Termux without root access.

![TermuxConf Banner](banner.png)

### Features

- **Web-based interface** — manage Termux settings in your browser.
- **General settings** — edit supported options using switches, selection lists, and input fields.
- **Hardware keyboard shortcuts** — enable or disable shortcuts and customize their key combinations.
- **Extra Keys editor** — visually configure key layouts, labels, actions, macros, and popup actions.
- **Automatic backups** — create dated backups at startup and before saving or restoring a configuration.
- **Restore previous configurations** — choose a dated backup to recover an earlier setup.
- **Preserve existing configuration** — retain unrelated settings and comments when saving changes.
- **Automatic reload** — reload Termux settings after saving when supported by the environment.
- **No root required** — intended for a standard Termux installation.

## Installation

1. Install [Termux](https://termux.dev/) if it is not already installed.
2. Ensure that **Python 3** is available in Termux. If needed, install it with:

   ```bash
   pkg install python
   ```

3. Download `TermuxConf.sh` and `banner.png` from this repository, keeping the banner in the same directory as the script if you want to use it in your project page or documentation.
4. Open Termux and navigate to the directory containing `TermuxConf.sh`.
5. Make the script executable:

   ```bash
   chmod +x TermuxConf.sh
   ```

6. Start TermuxConf:

   ```bash
   ./TermuxConf.sh
   ```

## Usage

Start the script from Termux:

```bash
./TermuxConf.sh
```

The script displays the local web address and port. Open that address in your browser to use the interface. The default bind address is `127.0.0.1`, so the interface is intended for access from the same device.

In the interface, review the available settings, make your changes, and save them. You can also create a manual backup or select a dated backup to restore an earlier configuration.

### Command-line options

```text
-p, --port <number>   Choose the web server port (1024–65535).
-a, --addr <IPv4>     Choose the IPv4 bind address (default: 127.0.0.1).
-c, --clean           Delete old backups.
-h, --help            Show help.
-v, --version         Show the version.
```

For example, to select a specific port:

```bash
./TermuxConf.sh --port 8080
```

**Security note:** Binding to an address other than `127.0.0.1` may allow other devices on the network to reach the configuration interface. Only do this on a trusted network and when you understand the exposure.

**Tip:** Keep a backup before making major changes. Some settings may require reloading the Termux configuration to take effect.

## Support

### Contact me:

For any issues, suggestions, or questions, reach out via:

- *Email:* support@burixon.dev
- *Contact form:* [Click here](https://burixon.dev/contact/)
- *Bug reports:* [Click here](https://burixon.dev/bugreport/#TermuxConf)

### Support me:

If you find this script useful, consider supporting my work by making a donation:

[**Donations**](https://burixon.dev/donate/)

Your contributions help in developing new projects and improving existing tools!

## License

TermuxConf is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. See the [official license text](https://www.gnu.org/licenses/agpl-3.0.html) for the full terms.
