# Setup GitHub MCP in Cursor

This guide explains how to set up and use the GitHub MCP integration in Cursor.

## Step-by-Step Setup Instructions

### 1. Create a GitHub Personal Access Token (Classic Token)

* Go to your GitHub account settings
* Navigate to `Developer Settings` > `Personal Access Tokens` > `classic-token`
* Click "Generate new token"
* Give your token a descriptive name
* Set an expiration date
* Select the repositories you want to grant access to
* Configure permissions (recommended to give only the minimum necessary permissions)
* Click "Generate token"
* Copy your token (you'll need it in step 2)

### 2. Set Up Smithery.ai GitHub MCP

* Go to [Smithery.ai](https://smithery.ai)
* Log in with your GitHub account
* Navigate to their GitHub MCP server section
* During installation, look for the "Cursor" tab
* Paste your GitHub Personal Access Token from step 1
* The site will generate a command - copy this command

### 3. Configure Cursor

* Open Cursor
* Go to `Settings` (gear icon)
* Navigate to the `MCP` section
* Click "+ Add new global MCP server"
* This will create or open an `mcp.json` file
* In the command field, paste:

    ```json
    {
      "mcpServers": {
        "Github": {
          "command": <PASTE YOUR COMMAND>
        }
      }
    }
    ```

    (Replace `<PASTE YOUR COMMAND>` with the command you copied from Smithery.ai)

## Using GitHub MCP in Cursor

Once configured, you can use the Cursor Agent tab to:

* Create new repositories
* Make changes to existing repositories
* Push code directly from Cursor with the help of Cursor Agent
* And more!

## Important Notes

* Regularly rotate your access tokens for security
* Check Smithery.ai documentation for the latest features and commands
