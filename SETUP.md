# Set up Pi Security for Grok

The Pi Security plugin uses browser-based sign-in to connect Grok to Pi Security. The plugin does not include any credentials.

## Before you begin

Install Grok Build by following xAI's [official installation instructions](https://docs.x.ai/build/overview#install). If Grok is already installed, update it with:

```shell
grok update
```

This plugin does not require a specific Grok version. Confirm that your installation includes plugin management:

```shell
grok version
grok plugin --help
```

You also need a Pi Security account with access to at least one tenant.

## 1. Install the plugin

Run these commands in your terminal:

```shell
grok plugin marketplace add pi-sloane/grok-plugin
grok plugin install pi-security --trust
```

The `--trust` option skips Grok's installation trust prompt. Browser sign-in in the next step connects Grok to Pi Security.

## 2. Sign in

Start a new Grok session and open `/mcps`. Select `pi-security`, then follow the authentication prompt. Grok will open Pi Security's sign-in flow in your browser.

If you can access more than one Pi Security tenant, choose the tenant you want to use. Grok may also ask you to sign in the first time you use the plugin.

## 3. Confirm your connection

Ask Grok:

> Which Pi Security account and tenant am I connected to?

The plugin will show details about the connection, including the tenant and permissions, without exposing your credentials. If you have access to multiple tenants, confirm that the correct one is selected before continuing.

Your tenant is selected when you sign in. Changing repositories or working directories does not change that selection.

## Troubleshooting

### Grok or plugin commands are unavailable

Follow xAI's [installation instructions](https://docs.x.ai/build/overview#install), or run `grok update` for an existing installation. Then confirm that `grok plugin --help` succeeds.

### The marketplace or plugin does not appear

Check the configured marketplaces and installed plugins:

```shell
grok plugin marketplace list
grok plugin list
```

If the Pi Security marketplace is missing, run the marketplace-add command from step 1 again. If the plugin is installed but needs an update, run:

```shell
grok plugin update pi-security
```

### Pi Security does not connect

Run Grok's MCP diagnostic command:

```shell
grok mcp doctor pi-security
```

Then open `/mcps`, select `pi-security`, and press `i` to sign in again. See xAI's [MCP server troubleshooting guide](https://docs.x.ai/build/features/mcp-servers#troubleshooting) for more detail.

## Reconnect or disconnect

Open `/mcps`, select `pi-security`, and use the authentication controls to reconnect or clear the saved sign-in.

To remove the plugin from Grok, run:

```shell
grok plugin uninstall pi-security
```

Disconnecting or uninstalling the plugin does not delete your Pi Security account or any data stored in Pi Security.
