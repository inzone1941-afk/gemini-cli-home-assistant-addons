# Gemini CLI Terminal for Home Assistant

[![License][license-shield]][license]
[![Maintainer][maintainer-shield]][maintainer]

A secure, web-based terminal with the Google Gemini CLI pre-installed for Home Assistant.

![Gemini CLI Terminal Screenshot](https://github.com/inzone1941-afk/gemini-cli-home-assistant-addons/raw/main/gemini-terminal/screenshot.png)

*Gemini CLI Terminal running in Home Assistant*

## What is Gemini CLI Terminal?

This add-on provides a web-based terminal interface with the Google Gemini CLI pre-installed, allowing you to use Gemini's powerful AI capabilities directly from your Home Assistant dashboard. It gives you direct access to Google's Gemini AI assistant through a terminal, ideal for:

- **🏠 Smart Home Control**: Use natural language to control devices via the built-in Home Assistant MCP server.
- **💻 Coding Assistant**: Get help with Home Assistant YAML, Python scripts, and complex automations.
- **🔍 Advanced Debugging**: Analyze Home Assistant logs and troubleshoot issues with AI assistance.
- **🧠 System Awareness**: Gemini automatically understands your entities, system info, and recent logs through "Smart Context".

## Key Features

- **🚀 Auto-Launch & Session Picker**: Starts Gemini automatically or provides a menu to continue previous sessions.
- **🔗 Deep Home Assistant Integration**: Pre-configured [ha-mcp](https://github.com/homeassistant-ai/ha-mcp) for native control of your home.
- **📝 Smart Context**: Automatically generates a `GEMINI.md` file with your system state for the AI to read.
- **🛡️ Secure Headless Auth**: Use your `gemini_api_key` for zero-config, persistent authentication.
- **📦 Persistent Packages**: Install APT and PIP packages that survive container restarts.
- **🎨 Polished UI**: High-performance terminal (`ttyd`) with support for themes (Breeze, Dracula, Nord, etc.).
- **🔄 Session Persistence**: Built-in `tmux` ensures your sessions stay alive even if you close the browser.

## Quick Start

The terminal automatically starts Gemini when you open it. You can immediately start using commands like:

```bash
# Ask Gemini about your smart home
gemini "Is the coffee maker on?"

# Start an interactive coding/chat session
gemini

# Resume your last conversation
gemini -c

# Refresh the AI's understanding of your system
ha-context
```

## Installation

1. Add this repository to your Home Assistant: 
   `https://github.com/inzone1941-afk/gemini-cli-home-assistant-addons`
2. Install the **Gemini CLI Terminal** add-on.
3. (Optional) Enter your **Gemini API Key** in the **Configuration** tab for a seamless experience.
4. Start the add-on.
5. Click **OPEN WEB UI** or use the sidebar icon.

## Configuration

| Option | Default | Description |
|--------|---------|-------------|
| `gemini_api_key` | `""` | Your Google Gemini API Key. |
| `auto_launch_gemini` | `true` | Automatically start Gemini on terminal open. |
| `enable_ha_mcp` | `true` | Enable the Home Assistant MCP server integration. |
| `ha_smart_context` | `true` | Automatically generate a system context file (`GEMINI.md`). |
| `persistent_apt_packages` | `[]` | List of Debian (APT) packages to install on startup. |
| `persistent_pip_packages` | `[]` | List of Python (PIP) packages to install on startup. |
| `terminal_theme` | `breeze` | Visual theme for the terminal (Breeze, Dracula, Nord, etc.). |

## Credits & Inspiration

This project is a refitted fork of the **[Claude Terminal for Home Assistant](https://github.com/heytcass/home-assistant-addons)** by **[Tom Cassady (@heytcass)](https://github.com/heytcass)**. 

Special thanks to the original author for the excellent foundation and to the **[OpenCode](https://github.com/magnusoverli/opencode)** project for architectural inspiration.

## License

This project is licensed under the MIT License - see the [LICENSE](../LICENSE) file for details. Gemini CLI is subject to Google's Terms of Service.

[license-shield]: https://img.shields.io/github/license/inzone1941-afk/gemini-cli-home-assistant-addons.svg
[license]: https://github.com/inzone1941-afk/gemini-cli-home-assistant-addons/blob/main/LICENSE
[maintainer-shield]: https://img.shields.io/badge/maintainer-inzone1941--afk-blue.svg
[maintainer]: https://github.com/inzone1941-afk
