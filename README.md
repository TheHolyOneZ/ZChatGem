# ZChatGem
ZChatGem is a comprehensive Discord bot that enables AI-powered conversations using Google's Gemini API. It features a sophisticated persona system, advanced session management, usage tracking, and extensive customization options. The bot creates private chat channels for users to interact with customizable AI personalities.


> 💡 **Built for the Zygnal Ecosystem — to download and use this extension, you must be part of the Zygnal Ecosystem.**  
> This extension (cog) is part of the **Zygnal Ecosystem** and is only available through its supported platforms.  
> You can use it with:  
> - The **[Discord Bot Framework](https://github.com/TheHolyOneZ/discord-bot-framework)** — ideal for developers who want full control and flexibility *(includes an integrated extension marketplace)*, or  
> - The **[ZygnalBot](https://zygnalbot.de)** — a prebuilt, plug-and-play Discord bot *(also includes an integrated extension marketplace)*.  
>
> Browse and install extensions at [zygnalbot.com/extension](https://zygnalbot.com/extension).  
> For help or community discussions, join us on Discord: [discord.gg/sgZnXca5ts](https://discord.gg/sgZnXca5ts)



# ZChatGem - Advanced AI Chat System for Discord

## Overview

ZChatGem is a comprehensive Discord botcog that enables AI-powered conversations using Google's Gemini API. It features a sophisticated persona system, advanced session management, usage tracking, and extensive customization options. The bot creates private chat channels for users to interact with customizable AI personalities.

---

## Table of Contents

- [Key Features](#key-features)
- [Getting Started](#getting-started)
- [Admin Panel](#admin-panel)
- [Persona Management](#persona-management)
- [Usage Limits & Role System](#usage-limits--role-system)
- [Session Management](#session-management)
- [Publishing the Chat Launcher](#publishing-the-chat-launcher)
- [Analytics & Logging](#analytics--logging)
- [User Experience](#user-experience)
- [Advanced Configuration](#advanced-configuration)
- [Troubleshooting](#troubleshooting)

---

## Key Features

### 🎭 Persona System
- **Unlimited Personas**: Create as many AI personalities as needed
- **Customizable Personalities**: Define unique system prompts, greetings, and behaviors for each persona
- **Model Selection**: Choose from multiple Gemini models per persona (gemini-2.5-pro, gemini-2.5-flash, gemini-2.0-flash-exp, and more)
- **Independent Configurations**: Each persona can have its own temperature, token limits, and generation parameters
- **Custom Greetings**: Set personalized welcome messages for each AI personality
- **Fixed or Global Limits**: Choose between persona-specific limits or server-wide/role-based limits

### 🔒 Advanced Session Management
- **Private Chat Channels**: Each conversation creates a dedicated, private channel
- **Persistent Sessions**: Sessions survive bot restarts and are automatically restored
- **Configurable Timeouts**: Set custom inactivity timeouts (default: 30 minutes)
- **Timeout Warnings**: Users receive warnings 5 minutes before session expiration
- **Auto-Delete Channels**: Optionally delete channels automatically when sessions end
- **Real-time Updates**: Session information updates every 8 seconds with current usage stats
- **Context Retention**: Maintains conversation history within configurable context windows
- **User Cooldowns**: 3-second cooldown between messages to prevent spam

### 📊 Usage Tracking & Limits
- **Dual Limit Systems**:
  - **Global Limits**: Server-wide message and token limits
  - **Role-Based Limits**: Bonus limits for specific roles
  - **Persona-Fixed Limits**: Individual limits per persona (overrides global/role limits)
- **Time-Based Tracking**: Daily and weekly message limits
- **Token Counting**: Accurate tracking of API token usage
- **Real-time Monitoring**: Live usage statistics displayed in chat sessions
- **Historical Analytics**: 90-day retention of usage data with automatic cleanup

### 🎨 Complete Customization
- **Embed Designer**: Customize title, description, color, thumbnail, and footer
- **Button Configuration**: Modify label, emoji, and style (primary/secondary/success/danger)
- **Dropdown Menu**: Customize placeholder text for persona selection
- **Response Formatting**: Choose between plain text or embedded responses
- **Typing Indicators**: Toggle visual "bot is typing" indicators

### 🔐 Security & Privacy
- **Per-Guild API Keys**: Each server has its own encrypted Gemini API key
- **Fernet Encryption**: 256-bit encryption for all stored API keys
- **Private Sessions**: Only the user who started a session can access their chat
- **Role-Based Access Control**: Restrict specific personas to certain roles
- **Secure Key Storage**: Keys stored in guild-specific folders with individual encryption

### 📈 Analytics & Reporting
- **Comprehensive Statistics**: Track messages, tokens, and sessions
- **Daily Reports**: View usage for the current day
- **Weekly Reports**: Analyze trends over the past week
- **Top Performers**: See most-used personas and most active users
- **Real-time Metrics**: Monitor last 10 minutes of activity
- **Custom Logs Channel**: Direct analytics to a dedicated channel

---

## Getting Started

### Initial Setup

1. **Add the Bot**: Invite ZChatGem to your Discord server with appropriate permissions:
   - Manage Channels
   - Send Messages
   - Embed Links
   - Manage Messages
   - Read Message History

2. **Set Up API Key**: Obtain a Gemini API key from [Google AI Studio](https://makersuite.google.com/app/apikey)

3. **Configure the Bot**: Use the `/zchatgem` command to open the admin panel

### First-Time Configuration Checklist

✅ Set your Gemini API key in the API Key tab
✅ Create at least one persona in the Personas tab
✅ Configure global usage limits in the Limits tab
✅ Customize the chat launcher design in the Design tab
✅ Select a publish channel in the Publish tab
✅ Publish your chat launcher

---

## Admin Panel

The admin panel is accessed via the `/zchatgem` or `!zchatgem` command and requires **Manage Server** permissions.

### Panel Navigation

The panel features 8 tabs organized in two rows:

**Row 1:**
- 🎨 **Design** - Customize chat launcher appearance
- 🧠 **Personas** - Create and manage AI personalities
- ⚖️ **Limits** - Configure usage restrictions
- 👥 **Roles** - Manage role-specific permissions

**Row 2:**
- ⚙️ **Settings** - Configure bot behavior
- 🚀 **Publish** - Deploy chat launcher
- 🔑 **API Key** - Manage Gemini API credentials
- 📊 **Logs** - View analytics and reports

### Design Tab

**Embed Configuration:**
- **Title**: Main heading for the chat launcher (max 256 characters)
- **Description**: Explanatory text about the chat system (max 4000 characters)
- **Color**: Hex color code for embed border (e.g., 5865F2)
- **Thumbnail**: Optional image URL
- **Footer**: Credit text at bottom of embed (max 2048 characters)

**Button Configuration:**
- **Label**: Text displayed on buttons (max 80 characters)
- **Emoji**: Optional emoji prefix
- **Style**: Visual appearance (primary/secondary/success/danger)

**Dropdown Configuration:**
- **Placeholder**: Text shown before selection (max 100 characters)

---

## Persona Management

### Creating a Persona

1. Navigate to the **Personas** tab
2. Click **Create Persona**
3. Fill in the modal:
   - **Name**: Display name for the AI (max 100 characters)
   - **System Prompt**: Personality and behavior instructions (max 2000 characters)
   - **Greeting**: Welcome message when chat starts (max 1000 characters)

### Configuring Persona Settings

After creation, click **Manage Personas** → **Edit This** to access:

**Name/Prompt/Greeting:**
- Modify the persona's core identity and behavior
- Update welcome messages
- Refine system prompts for better responses

**Model/Limits:**
- **Model Name**: Select from available Gemini models
  - gemini-2.5-pro (Most capable)
  - gemini-2.5-flash (Fast and efficient)
  - gemini-2.0-flash-exp (Experimental features)
  - gemini-2.0-flash-lite (Lightweight)
  - And more variants
- **Max Output Tokens**: Control response length (typically 2048-8192)
- **Temperature**: Creativity level (0.0-1.0, default 0.7)
  - Lower = More focused and deterministic
  - Higher = More creative and varied
- **Max Daily Messages**: Limit for fixed persona limits
- **Use Fixed Limits**: Toggle between persona-specific or global/role limits

### Advanced Persona Features

**Context Understanding:**
- Personas maintain conversation history based on context window settings
- System prompts define personality, knowledge domain, and response style
- Greetings set the tone for initial interactions

**Model Comparison:**
- **Pro Models**: Best for complex reasoning and detailed responses
- **Flash Models**: Optimized for speed and efficiency
- **Lite Models**: Minimal resource usage for simple tasks

### Managing Multiple Personas

- **Navigation**: Use Previous/Next arrows to browse personas
- **Quick Stats**: View ID, model, limit type, and daily message count
- **Bulk Management**: Up to 5 personas shown per page in main tab
- **Deletion**: Permanent removal with confirmation (cannot be undone)

---

## Usage Limits & Role System

### Global Limits (Server-Wide)

Set baseline limits for all users:
- **Daily Messages**: Maximum messages per user per day (default: 100)
- **Weekly Messages**: Maximum messages per user per week (default: 500)
- **Max Tokens**: Maximum tokens per response (default: 8192)

### Role-Based Bonus Limits

Grant additional limits to users with specific roles:

**Configuration:**
1. Navigate to **Limits** tab → **Add Role Limit**
2. Enter Role ID (right-click role in Discord with Developer Mode enabled)
3. Set bonus daily messages (e.g., +50)
4. Set bonus weekly messages (e.g., +200)
5. Optionally specify allowed/blocked gems (persona IDs)

**How Bonuses Work:**
- Bonuses stack with global limits
- Multiple roles = cumulative bonuses
- Example: Global 100 + Role A (+50) + Role B (+25) = 175 daily messages

### Persona-Fixed Limits

Override global/role limits for specific personas:

**When to Use:**
- Premium personas with restricted access
- High-token-usage models requiring tighter control
- Special event personas with temporary limits

**Configuration:**
- Set "Use Fixed Limits" to "true" in persona configuration
- Define daily/weekly message caps
- These limits ignore global and role bonuses

### Role-Based Persona Access

**Allowed Gems:**
- Specify which personas a role can access
- Empty list = all personas allowed
- Comma-separated persona IDs

**Blocked Gems:**
- Prevent specific personas from being used by a role
- Takes priority over allowed gems
- Useful for restricting powerful models

### Viewing Role Details

Access comprehensive role information:
- Daily and weekly bonuses
- List of allowed personas (by name)
- List of blocked personas (by name)
- Navigate between configured roles

---

## Session Management

### How Sessions Work

1. **Initiation**: User selects persona from published launcher
2. **Channel Creation**: Bot creates private text channel (`ai-chat-001-username`)
3. **Welcome Message**: Initial embed with persona greeting and usage stats
4. **Conversation**: User sends messages, AI responds with context awareness
5. **Termination**: User clicks "Close Chat" or session times out

### Session Features

**Privacy:**
- Channels are private by default
- Only the user who started the session can read/write
- Server admins with "Manage Channels" can still view

**Real-Time Updates:**
- Welcome message updates every 8 seconds
- Shows current token usage
- Displays daily/weekly message counts
- Calculates remaining messages

**Context Management:**
- Maintains conversation history in memory
- Configurable context window (default: 20 messages)
- Automatic pruning when context exceeds 2x window size
- Full conversation stored in database

**Close Chat Button:**
- Always visible in welcome message
- Ends session immediately
- Optionally deletes channel (configurable)
- Saves analytics before closure

### Session Timeout System

**Configurable Duration:**
- Default: 30 minutes of inactivity
- Customizable in Settings tab

**Warning System:**
- At 25 minutes: "This chat will close in X minutes due to inactivity"
- Sent to chat channel
- Resets if user sends a message

**Timeout Actions:**
- Session data saved to database
- Channel automatically deleted (if enabled)
- Analytics logged
- Memory cleaned up

### Session Persistence

**Across Bot Restarts:**
- All active sessions stored in SQLite database
- Automatic restoration on bot startup
- Session state includes:
  - User ID and Persona ID
  - Full conversation context
  - Token/message counts
  - Creation and last activity timestamps
  - Welcome message ID for updates

**Cleanup:**
- Timed-out sessions removed after timeout period
- Deleted channels trigger session cleanup
- 90-day analytics retention, then auto-delete

### Channel Management

**Auto-Delete Feature:**
- Configurable in Settings tab (true/false)
- When enabled: Channels deleted on session close
- When disabled: Channels remain, session still ends

**Permission Handling:**
- Bot requires "Manage Channels" permission
- If missing: Error message to user, manual cleanup required
- Overwrites ensure only participant can access

---

## Publishing the Chat Launcher

### Publishing Process

1. **Select Channel**:
   - Navigate to Publish tab
   - Click "Select Channel"
   - Mention channel in chat (e.g., `#general`) or paste channel ID
   - Bot confirms channel selection

2. **Verify Readiness**:
   - ✅ API Key: Must be set
   - ✅ Personas: At least one persona created
   - ✅ Channel: Valid channel selected

3. **Publish**:
   - Click "Publish Now"
   - Bot sends embed to selected channel
   - Dropdown menu populated with available personas
   - Users can now start chats

### Chat Launcher Components

**Embed Display:**
- Title and description from Design tab
- Color scheme matching configuration
- Optional thumbnail image
- Footer with credits

**Persona Dropdown:**
- Lists all created personas
- Shows persona name as label
- System prompt preview as description (first 100 chars)
- Single-select menu

**User Interaction:**
1. User opens dropdown
2. Selects desired persona
3. Bot checks permissions and limits
4. Creates private channel if authorized
5. Initiates chat session

### Publishing Management

**Unpublishing:**
- Click "Unpublish" in Publish tab
- Removes chat launcher message
- Does not affect active sessions
- Can republish at any time

**Updating:**
- Republishing overwrites previous launcher
- Updates design changes automatically
- New personas appear immediately
- Old launcher message deleted

**Multi-Channel Publishing:**
- Can only publish to one channel at a time
- Republishing changes target channel
- Previous channel launcher removed

---

## Analytics & Logging

### Available Reports

**Daily Report:**
- Total messages and tokens for current day
- Top 5 most-used personas with usage stats
- Accessible via Logs tab → "Daily Report"

**Weekly Report:**
- Cumulative stats since Monday (week start)
- Top 5 personas by usage
- Top 5 users by message count
- Comprehensive overview of weekly activity

**Live Logs:**
- Top 5 users by total messages
- Top 5 personas by total messages
- Based on all-time analytics data

### Real-Time Statistics

**Logs Tab Dashboard:**
- **Overall Statistics**:
  - Total sessions created
  - Total messages sent
  - Total tokens consumed
  - Average tokens per message
- **Today's Activity**:
  - Messages today
  - Tokens today
  - Currently active chats
- **Last 10 Minutes**:
  - Recent message count
  - Recent token usage
- **This Week**:
  - Weekly message total
  - Weekly token total
- **Top Performer**:
  - Most-used persona (by messages)

### Setting Up Logs Channel

1. Navigate to Logs tab
2. Click "Set Logs Channel"
3. Mention channel or paste ID
4. Bot confirms configuration

**Future Use:**
- Automated report posting
- Real-time alerts for limits
- Error notifications

### Data Retention

**Analytics Storage:**
- Daily/weekly/total statistics
- Per-user, per-persona breakdowns
- 90-day automatic retention
- Older data automatically purged

**Session Data:**
- Active sessions in memory and database
- Completed sessions archived
- Context and token counts preserved

**Backup System:**
- Daily database backups
- Stored in `data/zchatwithgemini/backups/`
- Format: `{guild_id}_{YYYYMMDD}.sqlite`

---

## User Experience

### Starting a Chat

1. Navigate to channel with published launcher
2. Click dropdown menu
3. Select desired AI persona
4. Read ephemeral message with channel link
5. Navigate to private channel
6. Begin conversation

### During Conversation

**Sending Messages:**
- Type normally in the private channel
- 3-second cooldown between messages (prevents spam)
- Bot shows typing indicator (if enabled)
- Responses typically arrive within 5-30 seconds

**Welcome Message Updates:**
- Refreshes every 8 seconds
- Shows real-time usage stats
- Updates token count after each message
- Always shows Close Chat button

**Context Awareness:**
- AI remembers previous messages in conversation
- Context window: last 20 messages (configurable)
- Maintains coherent, flowing conversation
- References earlier topics naturally

### Response Handling

**Standard Responses:**
- Plain text by default
- Embed format if configured in Settings

**Long Responses:**
- Messages over 2000 characters automatically split
- Sent as multiple messages (1900 char chunks)
- Maintains readability and formatting

**Error Responses:**
- "⏳ Rate limit exceeded" - Wait and retry
- "❌ Invalid request" - Model doesn't support input
- "❌ API key invalid" - Contact server admin
- "❌ Request timed out" - Try again

### Closing a Session

**Manual Closure:**
1. Click "Close Chat" button in welcome message
2. Bot confirms closure
3. Channel deleted (if auto-delete enabled) or session ends

**Automatic Closure:**
- Timeout after inactivity period
- Warning at 25 minutes of inactivity
- Channel auto-deleted if configured

### Usage Limit Notifications

**When Limits Reached:**
- Embed shows daily/weekly limit status
- Red warning embed appears
- Close Chat button provided
- Session ends automatically

---

## Advanced Configuration

### Settings Tab

**Context Settings:**
- **Context Window Size**: Number of messages AI remembers (default: 20)
  - Lower = Less memory, faster responses, lower token usage
  - Higher = Better context, slower responses, higher token usage
- **Smart Context**: Always enabled (automatic optimization)
- **Token Tracking**: Always enabled (accurate usage monitoring)

**Session Settings:**
- **Timeout**: Minutes before inactive sessions close (default: 30)
- **Auto Delete Channels**: Remove channels when sessions end (true/false)
- **Embed Responses**: Format AI responses as embeds (true/false)

**UI Settings:**
- **Typing Indicator**: Show "bot is typing" animation (true/false)
- **Long Message Split**: Always enabled (prevents Discord limits)
- **Error Messages**: Always detailed (helps with troubleshooting)

### API Key Management

**Setting API Key:**
1. Navigate to API Key tab
2. Click "Set API Key"
3. Paste your Gemini API key (39-60 characters)
4. Bot encrypts and stores key

**Key Security:**
- Per-guild encryption (each server separate)
- Fernet 256-bit encryption
- Keys stored in guild-specific folders
- Never transmitted in plain text

**Removing API Key:**
- Click "Remove API Key" in API Key tab
- Permanently deletes encrypted key
- Disables all AI functionality
- Does not affect persona configurations

**Key Scope:**
- Each Discord server has its own API key
- API keys are not shared between servers
- Allows different billing/limits per server

### Owner Commands

**`!geminitest` Command** (Bot Owner Only):
- Tests all available Gemini models
- Checks API key validity
- Reports token usage per model
- Identifies rate limits or errors
- Environment variable `bot_owner_id` must be set

---

## Troubleshooting

### Common Issues

**"❌ API key not configured"**
- Solution: Set Gemini API key in API Key tab
- Verify key is valid from Google AI Studio

**"❌ You do not have permission to use this persona"**
- Cause: Role-based restrictions active
- Solution: Contact server admin to adjust role limits

**"⚠️ Usage Limit Reached"**
- Cause: Daily or weekly message limit exceeded
- Solution: Wait for limit reset (daily at midnight UTC, weekly on Monday)

**"❌ I do not have permissions to create channels"**
- Cause: Bot missing "Manage Channels" permission
- Solution: Grant permission in server settings

**"⏳ Rate limit exceeded"**
- Cause: Too many API requests to Gemini
- Solution: Wait 1-2 minutes and try again

**Bot not responding in session:**
- Check bot is online
- Verify API key is still valid
- Ensure bot has "Send Messages" permission in channel
- Check for typing indicator (indicates processing)

**Session not found after bot restart:**
- Timeout may have expired during downtime
- Channel may have been manually deleted
- Database corruption (rare) - contact admin

**Personas not appearing in dropdown:**
- Verify at least one persona created
- Check publish channel has correct launcher
- Try unpublishing and republishing

### Performance Optimization

**Reducing Token Usage:**
- Lower context window size (e.g., 10 messages)
- Use Flash or Lite models instead of Pro
- Set lower max output tokens
- Enable shorter system prompts

**Speeding Up Responses:**
- Use gemini-2.0-flash or flash-lite models
- Reduce max output tokens
- Lower context window
- Disable embed responses

**Managing Server Load:**
- Set stricter usage limits
- Implement role-based access
- Use persona-fixed limits for expensive models
- Monitor analytics regularly

### Getting Help

**Bug Reports:**
- Join official Discord: `.gg/sgZnXca5ts`
- Provide full error messages
- Include steps to reproduce
- Share relevant configuration (without API key)

**Feature Requests:**
- Submit via Discord community
- Explain use case clearly
- Describe expected behavior

**License Compliance:**
- Do not modify code (see license)
- Report bugs instead of fixing yourself
- Preserve all attribution and credits
- Do not redistribute bot files

---

## Credits & Attribution

**Created by:** TheHolyOneZ (TheZ)  
**AI Technology:** Powered by Google Gemini  
**Official Website:** zygnalbot.com/extension/  

**Important:** This bot uses Google's Gemini AI models. All AI-related credits must remain intact as per license requirements. Removing or altering attribution violates the license agreement.

---

## License Notice

This software is provided under a custom license. By using ZChatGem, you agree to:
- Not modify, edit, or alter the code
- Not redistribute or share the bot files
- Preserve all attribution and branding
- Report bugs to the original author
- Not create derivative works or competing products

For full license terms, see the LICENSE section in the source code.

---

## Quick Reference

### Admin Commands
- `/zchatgem` - Open admin panel (Requires: Manage Server)
- `/geminitest` - Test Gemini API models (Bot Owner Only)

### Key Permissions Required
- Manage Channels
- Send Messages
- Embed Links
- Manage Messages
- Read Message History

### Default Limits
- Daily Messages: 100 per user
- Weekly Messages: 500 per user
- Max Tokens: 8192 per response
- Session Timeout: 30 minutes
- Context Window: 20 messages
- User Cooldown: 3 seconds

### Supported Gemini Models
- gemini-2.5-pro
- gemini-2.5-flash
- gemini-2.5-flash-lite
- gemini-2.5-flash-preview-09-2025
- gemini-2.0-flash
- gemini-2.0-flash-exp
- gemini-2.0-flash-lite
- gemini-2.0-flash-lite-001

---

*This README covers all features and functionality of ZChatGem. For additional support, join the official Discord community.*
