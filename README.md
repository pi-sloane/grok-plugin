# Pi Security for Grok

Use Pi Security in Grok to investigate findings, review your security posture, and get remediation guidance as you work.

![Pi Security logo](assets/pi-favicon-light.svg)

This marketplace installs the official Pi Security plugin for Grok. The plugin connects to Pi Security through OAuth and does not install a local Pi service or include any credentials.

## What you can do

With the plugin, you can ask Grok to:

- Investigate, explain, summarize, and compare Pi Security findings.
- Review threat models and Code Gatekeeper results.
- Get remediation guidance for findings and vulnerable packages.
- Start a security design review.
- Import security reports written in Markdown.
- Find secure development guidance for the repository you're working in.

## Install the plugin

Run these commands in your terminal:

```shell
grok plugin marketplace add pi-sloane/grok-plugin
grok plugin install pi-security --trust
```

The first command adds the Pi Security marketplace. The second installs the plugin and allows Grok to connect to Pi Security.

Next, follow the sign-in and verification steps in [SETUP.md](SETUP.md).

## Safety and updates

Grok asks for your confirmation before using a Pi Security tool that changes data.

Each marketplace release points to a specific version of the public [`pi-sloane/claude-plugin`](https://github.com/pi-sloane/claude-plugin) repository. This keeps installations consistent and ensures that updates happen only when a new marketplace version is published.

## Privacy and support

Only share content that you are authorized to send to Pi Security, and never include credentials or secrets. Do not post customer information, private repository details, or other sensitive material in public issues or pull requests.

- [Privacy Policy](https://www.pi.security/privacy-policy)
- [Terms and Conditions](https://www.pi.security/terms-and-conditions)
- [Data Processing Agreement](https://www.pi.security/data-processing-agreement)
- [Report a security issue](SECURITY.md)
- Support: [contact@pi.security](mailto:contact@pi.security)

This marketplace is available under the [MIT License](LICENSE).
