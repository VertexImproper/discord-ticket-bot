# Discord Ticket Bot

A powerful and feature-rich Discord ticket bot with a beautiful GUI, dynamic panel management, and comprehensive admin controls.

## Features

🎫 **Dynamic Ticket Panel**
- Create beautiful ticket panels with customizable category buttons
- Automatically manages ticket channels in organized categories
- Responsive embed with sleek UI design

📝 **Core Commands**
- `/panel` - Send the main ticket panel to any channel
- `/ticketadmin add @user` - Add a user as ticket admin
- `/ticketadmin remove @user` - Remove a user from ticket admins
- `/ticketgui add [category]` - Add a new category button to the GUI
- `/ticketgui remove [category]` - Remove a category button from the GUI

🔐 **Admin Features**
- Manage ticket admin permissions
- Dynamically add/remove ticket categories without code changes
- Auto-create ticket categories
- Role-based access control
- Config-based system for easy customization

## Installation

### 1. Clone or Download the Repository
```bash
git clone https://github.com/VertexImproper/discord-ticket-bot.git
cd discord-ticket-bot
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure the Bot

Edit `config.json` and fill in your Discord bot details:

```json
{
  "token": "YOUR_BOT_TOKEN_HERE",
  "clientId": "YOUR_CLIENT_ID_HERE",
  "guildId": "YOUR_GUILD_ID_HERE",
  "staffRoleId": "STAFF_ROLE_ID_HERE",
  "ticketCategoryId": "",
  "ticketAdmins": [],
  "ticketGuiCategories": [
    "Support",
    "Staff-Apply",
    "Report",
    "Suggestion"
  ]
}
```

### 4. Register Slash Commands

```bash
node deploy-commands.js
```

### 5. Run the Bot

```bash
npm start
```

## Project Structure

```
discord-ticket-bot/
├── index.js                 # Main bot file
├── deploy-commands.js       # Command registration script
├── config.json               # Configuration file
├── package.json              # Dependencies
└── commands/                 # Slash commands folder
    ├── panel.js               # Panel command
    ├── ticketadmin.js         # Admin management command
    └── ticketgui.js           # GUI management command
```

## Usage Examples

### Send Ticket Panel
```
/panel
```
This sends a beautiful ticket panel to the current channel with buttons for all configured categories.

### Add Category to GUI
```
/ticketgui add Staff-Apply
```
Adds a new button labeled "Staff-Apply" to the ticket panel.

### Remove Category from GUI
```
/ticketgui remove Staff-Apply
```
Removes the "Staff-Apply" button from the ticket panel.

### Add Ticket Admin
```
/ticketadmin add @user
```
Grants a user ticket admin permissions.

## Configuration Details

- **token** - Your Discord bot token from Developer Portal
- **clientId** - Your bot's Client ID
- **guildId** - Your server's Guild ID (for slash commands)
- **staffRoleId** - Role ID for staff members (they'll see all tickets)
- **ticketCategoryId** - Auto-populated with the Tickets category ID
- **ticketAdmins** - Array of user IDs with admin permissions
- **ticketGuiCategories** - Array of category names for ticket buttons

## Getting Your IDs

1. **Bot Token & Client ID** - [Discord Developer Portal](https://discord.com/developers/applications)
2. **Guild ID** - Right-click your server name, copy Server ID (enable Developer Mode)
3. **Role ID** - Right-click a role, copy Role ID (enable Developer Mode)
4. **User ID** - Right-click a user, copy User ID (enable Developer Mode)

## Error Checking

✓ Permission validation on all admin commands
✓ Graceful error handling
✓ Console logging for debugging
✓ Config validation on startup
✓ Channel creation with proper permissions

## Requirements

- **Node.js** v16.0.0 or higher
- **discord.js** v14.0.0 or higher
- A Discord bot token
- Proper bot permissions (Manage Channels, Manage Roles, Send Messages, etc.)

## Support

For issues, suggestions, or questions:
- Open an Issue on GitHub
- Check existing documentation
- Review the bot's console logs for errors

## License

MIT License - Feel free to use this bot in your projects!

## Credits

Developed by **VertexImproper**
Powered by discord.js v14

---

**Made with ❤️ for the Discord community**
