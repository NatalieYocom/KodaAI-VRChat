# KODA-AI-VRChat

A very heavily modified version of [S0L0GUY/NOVA-AI](https://github.com/S0L0GUY/NOVA-AI), that allows the bot to interface with the OpenClaw framework, along with many other changes for personal use.

Planned Features:
- [ ]Report back events/memories to OpenClaw when finished
- [ ]Control of avatar accessories via OSC

Features

- Local memory system persisted in SQLite (`memories.db`)
- Audio input and output support
- Screenshot and basic vision logging
- Simple UI and command-line entry points

Requirements

- Python 3.11.9 recomended
- Dependencies listed in `requirements.txt`

Installation

1. Clone the repository and change into the project folder.

```bash
git clone https://github.com/NatalieYocom/KodaAI-VRChat
cd KodaAI—VRChat
```

2. Create and activate a virtual environment.

On Windows (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

On macOS or Linux:

```bash
python -m venv .venv
source .venv/bin/activate
```

3. Install Python dependencies.

```bash
pip install -r requirements.txt
```

Configuration

- Copy `config.yaml.example` to `config.yaml` and adjust settings as needed.
- Copy `prompt.yaml.example` to `prompt.yaml` and adjust wording as needed.
- Configure any API keys or local paths in `config.yaml`.
- Existing modules load from the `models/`, `sfx/`, and `tts_cache/` folders when applicable.
- The memory system persists data in a SQLite database at the configured `db_path`; by default, this is `memories.db` in the project root when memory is used.

Usage

- Run the main application:

```bash
python main.py
```

- Launch the alternative entry point:

```bash
python nova.py
```

- For a simple memory UI (if available):

```bash
python memory_ui.py
```

Project layout

```
.
├── classes/            # Core modules: audio, memory, UI, tools
├── json_files/         # JSON-based state and logs used by some modules
├── memories.db         # SQLite database used for persistent memory storage
├── models/             # Model files (not included)
├── sfx/                # Sound effects used by the app
├── tts_cache/          # Cached TTS audio
├── main.py             # Primary entry point
├── nova.py             # Alternate entry point
├── memory_ui.py        # Simple memory inspector UI
├── config.yaml         # Runtime configuration (not committed)
└── requirements.txt    # Python dependencies
```


Maintainers

- Natalie Yocom (SimplyNat)
