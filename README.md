# chat.sh - LLM Magic in Shell 🪄

A lightweight and elegant command-line interface for interacting with Cloudflare's AI models, featuring real-time Markdown rendering and a clean terminal UI.

## Features ✨

- Interactive chat interface with Cloudflare's LLaMA 3.2 11B Vision model
- Real-time Markdown rendering with syntax highlighting
- Clean and responsive terminal UI
- Support for streaming responses
- Token usage tracking
- Pipe input support for context injection

## Prerequisites 📋

- Bash shell environment
- Python 3.x
- `curl` command-line tool
- `jq` for JSON processing
- Python packages:
  - rich (for Markdown rendering)

## Installation 🚀

1. Clone the repository:

```bash
git clone https://github.com/ahmed-abdat/chat.sh.git
cd chat.sh
```

2. Create your `.id` file from the example:

```bash
cp .id.example .id
```

3. Edit `.id` with your Cloudflare credentials:

```bash
account_id="your_account_id"
auth="your_auth_token"
```

## Usage 💡

### Basic Usage

```bash
./chat.sh "Your question here"
```

### Interactive Mode

Simply run without arguments to enter interactive mode:

```bash
./chat.sh
```

### Pipe Input

You can pipe content to provide additional context:

```bash
cat file.txt | ./chat.sh "Explain this content:"
```

## Configuration ⚙️

- Model selection: Edit the `model` variable in `chat.sh`
- System prompt: Modify the `system_prompt` in `chat.sh`
- Token limit: Adjust `max_tokens` in `chat.sh`
- UI theme: Customize colors in `mdcat.py`

## How It Works 🔧

1. The main script (`chat.sh`):

   - Handles user input and API communication
   - Manages conversation context
   - Streams responses from the API
   - Tracks token usage

2. The renderer (`mdcat.py`):
   - Provides real-time Markdown rendering
   - Implements syntax highlighting
   - Handles terminal UI formatting
   - Manages display updates

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing 🤝

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## Acknowledgments 🙏

- Built on Cloudflare's AI platform
- Uses the Rich library for Python terminal formatting
- Inspired by modern CLI tools
