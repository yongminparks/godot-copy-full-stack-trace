# Copy Full Stack Trace - Godot Editor Plugin

A lightweight editor plugin for Godot that adds a **Copy Full**
button to the Debugger's **Stack Trace** panel. It collects the active error,
selected thread, and every stack frame into one clipboard-ready block of text.

![Godot 4.2+](https://img.shields.io/badge/Godot-4.2%2B-478CBF?logo=godotengine&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)

## Features

- Adds a **Copy Full** action directly to the Stack Trace panel
- Includes the active error or break reason
- Includes the currently selected thread
- Copies every frame in the displayed stack trace
- Formats frame numbers, file paths, line numbers, and function names

## Installation

### From the Godot Asset Library

1. Open the **AssetLib** tab in the Godot editor.
2. Search for **Copy Full Stack Trace**.
3. Click **Download**, then **Install**.
4. Open **Project → Project Settings → Plugins** and enable
   **Copy Full Stack Trace**.

### From GitHub

1. Copy this repository's `addons/copy-full-stack-trace/` folder into your
   project's `addons/` directory.
2. Open **Project → Project Settings → Plugins**.
3. Enable **Copy Full Stack Trace**.

Your project should contain:

```text
res://addons/copy-full-stack-trace/
├── LICENSE
├── plugin.cfg
└── plugin.gd
```

## Usage

1. Run or debug your project until execution stops on an error or breakpoint.
2. Open the **Debugger → Stack Trace** panel.
3. Select the thread whose trace you want to copy.
4. Click **Copy Full**.
5. Paste the result into an issue, chat, document, or debugging tool.

## Example output

```text
Invalid call. Nonexistent function 'attack' in base 'Nil'.
Thread: Main Thread

Stack Trace:
0 - res://player/player.gd:42 - at function: attack_target
1 - res://player/player.gd:18 - at function: _physics_process
```

## Compatibility

- Godot 4.2 or later
- Runs only in the editor; it is not included in exported games

The plugin integrates with Godot's built-in Stack Trace interface. A future
Godot editor UI change may require an update to the plugin.

## License

Copy Full Stack Trace is available under the [MIT License](LICENSE).
