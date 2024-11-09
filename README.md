Discord Bot - Multi-Tool Control Panel

Welcome to the Discord Bot Multi-Tool Control Panel! 🎉 This bot offers an array of powerful features designed to manage Discord servers effectively, providing streamlined control and flexibility. Here’s an overview of the key functionalities, installation instructions, and a breakdown of each option:
-----

-Remember to enable the option (Privileged Gateway Intents) in https://discord.com/developers/applications

-The index code is encrypted but don't worry, you can see the main operation of the code, I only care about not appropriating my work

 -----
 
🚀 Features & Options
-----

🤖 User Management

-List Users: Displays a list of all members in the selected server.

-Ban User: Bans a specified user by their ID.

-Mute User: Temporarily mutes a user for 10 minutes.

-Kick User: Removes a user from the server.

-Change User Nickname: Modifies the nickname of a specified user.
____
📁 Channel Management

-List Channels: Shows all text channels available on the server.

-Add Channels: Adds multiple new channels with optional automatic numbering.

-Delete Channels: Removes selected channels from the server.

-Rename Channel: Updates the name of an existing channel.
____
💬 Messaging

-Spam Messages: Sends a specified message multiple times in selected channels.

-Send Message to Channel: Directly posts a message to a specified channel.
____
🛠️ Role and Permission Management

-Create Role and Assign: Creates a new role with a specified color and assigns it to a user.

-Manage Write Access: Toggles a user’s permission to send messages in a particular channel.
____
📊 Polling and Voting

-Create Poll: Creates a poll with specified options for members to vote.
____
🔄 Undo Last Action

-Undo Action: Reverts the most recent action, where possible.
____


📥 Installation & Setup

-Create a new folder, place index.js in it and execute cmd commands in this folder:

cmd:

npm init -y or npm install

npm install inquirer@latest

npm install discord.js inquirer or npm install discord.js

Run the Bot:
node bot.js
----
Login Prompt:
On startup, the bot will prompt you to enter your bot's token.
----

📝 Code Breakdown

Token Initialization and Login
Upon launch, the bot prompts the user to enter the Discord token. This is handled through inquirer prompts.
Main Menu & Function Selection
Once logged in, the bot displays a menu where you can choose actions:
const action = await inquirer.prompt([ ... ]);
Each action maps to a specific function, offering options such as managing users, channels, roles, and more.
Channel and User Management
Actions like listing users, banning, or changing nicknames are managed through the Discord.js API using guild.members and guild.channels.
Undoing Actions
actionHistory stores actions, allowing selected actions to be undone, such as channel additions.
____
🛠 Technical Details
Packages Used
discord.js: For interaction with the Discord API.
inquirer: To create a command-line interface with options for easy selection and input.
Error Handling
Errors, especially during login or invalid actions, are caught and logged, ensuring smooth bot operation and easy debugging.
____
🔑 Permissions Required
The bot requires various permissions depending on the selected actions:

-Manage Messages: For messaging actions.

-Manage Channels: To create, delete, or rename channels.

-Manage Roles: For creating and assigning roles.

-Kick/Ban Members: Required for user moderation actions.

-Ensure the bot has these permissions on the selected server.

📝 Important Notes
----
The bot uses an in-memory action history to track actions, enabling selective undo. However, channel deletions cannot be reversed due to Discord's permanent delete policy.
Polls are limited to five options due to reaction limits on Discord messages.
Disclaimer
This bot is meant for educational purposes. Avoid using disruptive features like spamming in real servers without permission.
---
Happy Botting! 🚀
