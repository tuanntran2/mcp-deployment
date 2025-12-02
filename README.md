Use the following command to run the MCP server.
uvx  --from git+https://github.com/tuanntran2/mcp-deployment.git mcp-server

It's basically download the repository from github and run the mcp-server
which is defined in the pyproject.toml file.
[project.scripts]
mcp-server = "mcpserver.__main__:main"

To integrate this MCP into claude, add the following block into
claude_desktop_config.json file.

    "mcp-server": {
      "command": "uvx",
      "args": [
        "--from",
        "git+https://github.com/tuanntran2/mcp-deployment.git",
        "mcp-server"
      ]
    }