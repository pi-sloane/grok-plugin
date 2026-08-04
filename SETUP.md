# Set up Pi Security for Grok

The Pi Security plugin uses OAuth to connect Grok to Pi Security. You will sign in through Pi Security in your browser; the marketplace does not include or store your credentials.

## Before you begin

You need:

- A current version of Grok Build with plugin support.
- A Pi Security account with access to at least one tenant.

## 1. Install the plugin

Run these commands in your terminal:

```shell
grok plugin marketplace add pi-sloane/grok-plugin
grok plugin install pi-security --trust
```

Trusting the plugin allows Grok to connect to Pi Security's hosted service.

## 2. Sign in

Start a new Grok session and open `/mcps`. Select `pi-security`, then follow the authentication prompt. Grok will open Pi Security's sign-in flow in your browser.

If you can access more than one Pi Security tenant, choose the tenant you want to use. Grok may also ask you to sign in the first time you use the plugin.

## 3. Confirm your connection

Ask Grok:

> Which Pi Security account and tenant am I connected to?

The plugin will show details about the connection, including the tenant and permissions, without exposing your credentials. If you have access to multiple tenants, confirm that the correct one is selected before continuing.

Your tenant is selected when you sign in. Changing repositories or working directories does not change that selection.

## Reconnect or disconnect

Open `/mcps`, select `pi-security`, and use the authentication controls to reconnect or clear the saved sign-in.

To remove the plugin from Grok, run:

```shell
grok plugin uninstall pi-security
```

Disconnecting or uninstalling the plugin does not delete your Pi Security account or any data stored in Pi Security.
