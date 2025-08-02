# Frequently Asked Questions

## General Questions

### What is Mneme?

Mneme is a personal knowledge management system that helps you access your documents from any device. It uses Dropbox for synchronization and integrates with Claude Desktop for AI-powered assistance.

### Why use Mneme instead of just Dropbox?

Mneme adds:
- One-click access with desktop shortcuts
- Claude Desktop integration for AI assistance
- Notion upload preparation
- Automated setup and configuration

### Is Mneme free?

Yes, Mneme itself is free and open source. You'll need:
- Dropbox account (free tier works)
- Claude Desktop (optional)
- Notion account (optional)

## Setup Questions

### Can I change the document folder name?

Yes! Set the environment variable before running setup:
```bash
set MNEME_FOLDER_NAME=My_Custom_Folder
```

### What if I don't have Dropbox in the default location?

The script will prompt you to enter the path manually. You can also add custom paths to `config_local.json`.

### Do I need administrator rights?

Generally no, but you might need them for:
- Creating symbolic links (folder shortcuts)
- Modifying Claude Desktop configuration

### Can I use OneDrive/Google Drive instead of Dropbox?

Currently, Mneme is designed for Dropbox. However, you can modify the script to work with other services by changing the search paths.

## Usage Questions

### How do I add new documents?

Simply save files to your Mneme folder. They'll sync automatically via Dropbox.

### Can I organize documents in subfolders?

Yes! Create any folder structure you want within your Mneme folder.

### How do I access documents on mobile?

Use the Dropbox mobile app to view your documents. For editing, use any compatible app.

### What file types are supported?

Mneme works with any file type. For Claude Desktop:
- Text files (.txt, .md)
- Documents (.doc, .docx, .pdf)
- Code files
- And more

## Claude Desktop Questions

### Claude Desktop can't see my files

1. Restart Claude Desktop after setup
2. Check if MCP is configured correctly
3. Ensure the folder path doesn't contain special characters

### How do I use Claude with my documents?

After setup, just ask Claude:
- "Show me my recent notes"
- "Summarize the document about [topic]"
- "Help me find information about [subject]"

## Notion Questions

### How do I upload to Notion?

1. Run `Mneme_Notion_Prep.bat`
2. Open Claude Desktop
3. Ask Claude to upload the prepared files to your Notion database

### Can I use a different Notion database?

Yes, set the environment variable:
```bash
set MNEME_DATABASE_URL=https://www.notion.so/your_database_id
```

### What properties does the Notion database need?

Minimal requirements:
- Title (text)
- Content (rich text)
- Tags (multi-select) - optional

## Troubleshooting

### The setup script won't run

- Ensure Python 3.7+ is installed
- Check if Python is in your PATH
- Try `python3` instead of `python`

### Batch files show errors

- Check if paths contain spaces (they should be quoted)
- Ensure Dropbox sync is complete
- Verify Python installation

### Changes aren't syncing

- Check Dropbox sync status
- Ensure you have internet connection
- Verify you're editing files in the Mneme folder

## Privacy & Security

### Is my data safe?

- Mneme doesn't upload or store your data
- All sync happens through your Dropbox account
- Configuration is stored locally only

### Can others access my documents?

- Only if you share your Dropbox folder
- Claude Desktop access is local only
- Notion uploads require your explicit action

### What data does Mneme collect?

None. Mneme:
- Doesn't phone home
- Doesn't collect analytics
- Doesn't store personal information

## Advanced Questions

### Can I customize the setup process?

Yes, the script is open source. Feel free to modify it for your needs.

### How do I uninstall Mneme?

1. Delete desktop shortcuts
2. Remove `~/.mneme_setup_complete`
3. Remove `~/.mneme_tools/` folder
4. Optionally, remove Claude Desktop configuration

### Can I use Mneme on Linux/Mac?

The script is designed for Windows but can be adapted. Main changes needed:
- Path separators
- Desktop shortcut creation
- Claude Desktop configuration location