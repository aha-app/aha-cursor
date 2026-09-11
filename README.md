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

The plugin connects to `https://<subdomain>.aha.io/api/v1/mcp`. Authentication uses OAuth, so no API key is stored in this repository or entered into the plugin configuration.

To use a different Aha! account, update **Aha! account subdomain** under **Plugins → Configure**, then reconnect the MCP server.

## Local testing

Clone this repository, then link it into Cursor's local plugin directory:

```sh
mkdir -p ~/.cursor/plugins/local
ln -s "$(pwd)" ~/.cursor/plugins/local/aha
```

Restart Cursor or run **Developer: Reload Window**, then confirm that Aha! appears under **Customize** and that its MCP server can connect.

## License

This project is available under the [MIT License](LICENSE).
