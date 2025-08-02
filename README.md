# Mneme - Multi-Device Document Sync System

Mneme is a personal knowledge management system that synchronizes documents across multiple devices using Dropbox and integrates with Claude Desktop for AI-assisted access.

## Features

- 🔄 **Multi-device synchronization** via Dropbox
- 🤖 **Claude Desktop integration** for AI-powered document access
- 📚 **Notion database support** for persistent storage
- 🚀 **One-click setup** with standalone script
- 🔒 **Privacy-focused** - all personal data is configurable

## Quick Start

1. Download `mneme_standalone_setup.py`
2. Run: `python mneme_standalone_setup.py`
3. Follow the on-screen prompts
4. Double-click the created desktop shortcuts

## Requirements

- Python 3.7+
- Dropbox (installed and synced)
- Claude Desktop (optional, for AI features)
- Notion account (optional, for database storage)

## Configuration

### Environment Variables
```bash
# Set your document folder name
export MNEME_FOLDER_NAME="My_Documents"

# Set your Notion database URL
export MNEME_DATABASE_URL="https://www.notion.so/your_database_id"
```

### Configuration File
Create `config_local.json`:
```json
{
  "mneme_folder_name": "My_Documents",
  "notion_database_url": "https://www.notion.so/your_database_id",
  "dropbox_paths": [
    "~/Dropbox",
    "C:/Users/USERNAME/Dropbox"
  ]
}
```

## Project Structure

```
mneme/
├── mneme_standalone_setup.py    # Main setup script
├── config_example.json          # Configuration template
├── README.md                    # This file
└── LICENSE                      # MIT License
```

## How It Works

1. **Setup Phase**: The script detects your Dropbox folder and creates necessary shortcuts
2. **Daily Use**: Launch Mneme with one click to access your synchronized documents
3. **AI Integration**: Claude Desktop can directly access and help with your documents
4. **Cloud Backup**: Optionally upload to Notion for permanent storage

## Privacy & Security

- No hardcoded personal information
- All paths and IDs are configurable
- Local configuration files are gitignored
- You control where your data is stored

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - see LICENSE file for details

## Support

For issues and feature requests, please use the GitHub issue tracker.

---

*Mneme - Your thoughts, everywhere you need them.*