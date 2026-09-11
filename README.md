# Aha! for Cursor

Connect Cursor to your Aha! account through the official hosted Aha! MCP server. The plugin lets Cursor search, read, and manage the Aha! records you can access.

## Requirements

- An Aha! account with MCP access enabled
- An Aha! user with access to the AI assistant
- Your Aha! account subdomain — for example, `acme` for `acme.aha.io`

## Install and connect

1. Install **Aha!** from the Cursor Marketplace.
2. Enter your Aha! account subdomain when prompted.
3. Open the Aha! MCP server in Cursor and select **Connect**.
4. Complete the Aha! sign-in and authorization flow in your browser.

The plugin connects to `https://<subdomain>.aha.io/api/v1/mcp`.

## Local testing

Clone this repository, change into its root directory, then copy it into Cursor's local plugin directory. Use a real directory rather than a symlink so Cursor accepts the local plugin.

```sh
mkdir -p ~/.cursor/plugins/local
unlink ~/.cursor/plugins/local/aha 2>/dev/null || true
mkdir -p ~/.cursor/plugins/local/aha
rsync -a --exclude='.git/' ./ ~/.cursor/plugins/local/aha/
```

Restart Cursor or run **Developer: Reload Window**, then confirm that Aha! appears under **Customize → Plugins** and that its MCP server appears under **Customize → MCPs**.
