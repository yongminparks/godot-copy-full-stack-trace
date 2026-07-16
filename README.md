# Copy Full Stack Trace

A lightweight Godot 4 editor plugin that adds a **Copy Full** button to the
Debugger's **Stack Trace** panel. It collects the active error, selected thread,
and every stack frame into one clipboard-ready block of text.

![Godot 4.x](https://img.shields.io/badge/Godot-4.x-478CBF?logo=godotengine&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)

## Features

- Adds a **Copy Full** action directly to the Stack Trace panel
- Includes the active error or break reason
- Includes the currently selected thread
- Copies every frame in the displayed stack trace
- Formats frame numbers, file paths, line numbers, and function names

## Installation

1. Create `res://addons/copy_full_stack_trace/` in your Godot project.
2. Copy `plugin.cfg` and `plugin.gd` from this repository's `addons/` folder
   into that directory.
3. Open **Project > Project Settings > Plugins**.
4. Enable **Copy Full Stack Trace**.

Your project should contain:

```text
res://addons/copy_full_stack_trace/
├── plugin.cfg
└── plugin.gd
```

## Usage

1. Run or debug your project until execution stops on an error or breakpoint.
2. Open the **Debugger > Stack Trace** panel.
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

- Godot 4.x
- Runs only in the editor; it is not included in exported games

The plugin integrates with Godot's built-in Stack Trace interface. A future
Godot editor UI change may require an update to the plugin.

## License

Copy Full Stack Trace is available under the [MIT License](LICENSE).
