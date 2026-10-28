# Motorika plugin

Motorika gives a Claude Code agent fast, reliable control of Chrome over MCP: tabs, forms, clicks, video
frames, headed or headless. This plugin only registers the server; the code lives in
[X2Mobile/motorika-mcp](https://github.com/X2Mobile/motorika-mcp) and ships as the `motorika` npm package,
which the plugin runs with `npx -y motorika@<version>`.

## Install

Needs Node >= 20 and an installed Google Chrome. In Claude Code:

```
/plugin marketplace add X2Mobile/x2-plugins
/plugin install motorika@x2mobile
```

Run `/mcp` afterwards to see the server and its tools.

## Log in once

The agent uses its own Chrome profile, `~/.motorika/profile`. To sign in to sites the agent should use, open a
plain Chrome on that profile, sign in, then quit Chrome fully (Cmd+Q on macOS):

```sh
npx motorika open https://accounts.google.com
```

Keep your bank, your main email and admin accounts out of this profile. The full guide, flags and the safety
notes: [motorika-mcp docs](https://github.com/X2Mobile/motorika-mcp/tree/main/docs).

## Versions

The plugin version matches the npm version it runs (`.mcp.json` pins `motorika@0.1.0`). A new Motorika release
means bumping both here, then `/plugin marketplace update x2mobile`.
