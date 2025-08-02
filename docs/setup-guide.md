# Mneme Setup Guide

This guide walks you through setting up Mneme on your Windows machine.

## Prerequisites

1. **Python 3.7 or higher**
   - Download from [python.org](https://python.org)
   - Ensure Python is added to PATH

2. **Dropbox**
   - Install and sign in
   - Wait for initial sync to complete

3. **Claude Desktop** (Optional)
   - For AI-powered document access
   - Enable Notion integration if using

## Installation Steps

### Step 1: Download the Setup Script

Download `mneme_standalone_setup.py` to your computer (e.g., Desktop).

### Step 2: Configure Environment (Optional)

Set your preferences before running:

```bash
# Windows Command Prompt
set MNEME_FOLDER_NAME=My_Knowledge_Base
set MNEME_DATABASE_URL=https://www.notion.so/your_database_id

# Windows PowerShell
$env:MNEME_FOLDER_NAME = "My_Knowledge_Base"
$env:MNEME_DATABASE_URL = "https://www.notion.so/your_database_id"
```

### Step 3: Run the Setup

```bash
python mneme_standalone_setup.py
```

### Step 4: Follow the Prompts

The script will:
1. Search for your Dropbox folder
2. Create desktop shortcuts
3. Configure Claude Desktop (if installed)
4. Set up necessary tools

## What Gets Created

### Desktop Shortcuts

1. **Mneme_Launch.bat**
   - Opens your document folder
   - Starts Claude Desktop
   - One-click access to everything

2. **Mneme_Notion_Prep.bat**
   - Prepares documents for Notion upload
   - Shows database URL for reference

3. **Document Folder Shortcut**
   - Direct access to your synced documents

### Hidden Files

- `~/.mneme_setup_complete` - Setup completion marker
- `~/.mneme_tools/` - Standalone tools directory

## First Time Use

1. **Launch Mneme**
   - Double-click `Mneme_Launch.bat`
   - Your documents open automatically

2. **In Claude Desktop**
   - Say: "Show me the documents in the Mneme folder"
   - Claude will have access to your files

3. **Upload to Notion** (Optional)
   - Run `Mneme_Notion_Prep.bat`
   - Follow the instructions to upload via Claude

## Troubleshooting

### Dropbox Not Found

If the script can't find Dropbox:
1. Ensure Dropbox is running
2. Enter the path manually when prompted
3. Check if your documents folder exists

### Claude Desktop Not Configured

If Claude configuration fails:
1. Ensure Claude Desktop is installed
2. Restart Claude after setup
3. Manually add the folder in Claude settings

### Permission Errors

If you get permission errors:
1. Run Command Prompt as Administrator
2. Check folder permissions
3. Ensure antivirus isn't blocking

## Multi-Device Setup

To use Mneme on multiple devices:

1. **Ensure Dropbox is synced** on all devices
2. **Run the setup script** on each device
3. **Use the same folder name** (via environment variable)
4. **Documents sync automatically** via Dropbox

## Next Steps

- Create your first document in the Mneme folder
- Experiment with Claude Desktop integration
- Set up Notion database for cloud backup
- Customize your workflow

## Need Help?

Check the [FAQ](faq.md) or open an issue on GitHub.