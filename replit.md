# NyTier Discord Bot Project

## Overview
A Discord bot for managing player evaluation queues with role-based access control, persistent interactive buttons, and automated testing workflows. Built with Node.js and discord.js v14.

## Project Status
- **Created:** November 14, 2025
- **Status:** Development Complete - Ready for Testing
- **Stack:** Node.js v20, discord.js v14

## Features Implemented
1. `/setup` command - Configure queue, results, and control channels (Tester role required)
2. `/evaluate` command - Submit evaluation results with professional embeds
3. Queue system with 10-player limit and 8 gamemode options
4. Persistent control panel (Open/Close/Start Test/Kick buttons)
5. Persistent queue message (Join/Leave buttons) with live updates
6. Private ticket system for evaluations
7. Multi-server support with guild-specific configurations

## Architecture

### File Structure
```
/commands
  setup.js          - Channel configuration
  evaluate.js       - Evaluation submission
/utils
  configManager.js  - Config file operations
  queueManager.js   - In-memory queue state
/events
  interactionCreate.js - Button and command handling
  ready.js          - Bot initialization
index.js           - Main entry point
config.json        - Guild configurations
```

### Key Design Decisions
- In-memory queue storage (resets on restart, as specified)
- File-based configuration for persistence
- Persistent messages that update in place (no duplication)
- Role-based access using "Tester" role name
- Professional embed styling matching provided screenshots

## Setup Requirements

### Required Secrets
- `DISCORD_BOT_TOKEN` - Bot token from Discord Developer Portal
- `DISCORD_CLIENT_ID` - Application ID for command registration

### Discord Bot Setup
1. Create bot at https://discord.com/developers/applications
2. Enable SERVER MEMBERS INTENT and MESSAGE CONTENT INTENT
3. Generate bot token and client ID
4. Invite bot with administrator permissions
5. Create "Tester" role in Discord server

## User Preferences
- Language: Arabic (based on initial message)
- Style: Professional, clean embeds with emoji indicators
- No unnecessary comments in code (kept minimal)

## Recent Changes
- November 14, 2025: Initial project creation with complete bot functionality
