# GlassSSH Support

Welcome to the support repository for **GlassSSH**, a native SSH client for macOS. Use this repository to report bugs, request features, and ask questions about the app.

## About GlassSSH

GlassSSH brings your remote servers into one Mac workspace, with:

- Saved connection profiles, groups, tags, and favorites.
- Tabbed terminals and split panes for working across multiple sessions.
- An integrated SFTP browser for uploading and downloading files and folders.
- Password, interactive, and OpenSSH private-key authentication.
- Local, remote, and dynamic SSH tunnel configuration.
- JSON profile import and export without passwords or private-key contents.
- Quick Connect, keyboard shortcuts, and `glassssh://` connection links.
- Apple Keychain storage for secrets you explicitly choose to save.

GlassSSH requires **macOS 15 or later**, an SSH server, and valid credentials for that server.

## Get help

Open the **Issues** tab in this repository and search for an existing report or answer. If you cannot find one, create a new issue with a descriptive title and explain what you need help with.

Please write in English when possible so other users can benefit from the discussion. Keep each issue focused on one problem or request.

### Report a bug

Include the following details so the problem can be reproduced:

```text
Summary:

GlassSSH version:
Installation source (for example, Mac App Store or a local build):
macOS version:
Mac chip (Apple silicon or Intel):

Steps to reproduce:
1.
2.
3.

Expected behavior:

Actual behavior:

Error message, if any (remove sensitive information):

Additional context or screenshots:
```

For connection or file-transfer issues, also mention your authentication method, whether you use a jump host or tunnel, and whether the same connection works in another SSH client. Include the remote operating system and shell if relevant. You do not need to share the server's actual address or your credentials.

### Request a feature

Describe what you want to accomplish, what makes it difficult today, and how the proposed feature would help. Examples of your workflow are especially useful.

## Quick troubleshooting

### Unable to connect

- Check the hostname, port, username, and authentication method in the connection profile.
- Confirm that the server is reachable and that any required VPN is connected.
- If you use a private key, make sure you selected the correct OpenSSH key and that the matching public key is authorized on the server.
- Include the exact error message in your report, with sensitive details removed.

### Private keys or local folders are unavailable

In the sandboxed Mac App Store edition, select private keys and local transfer folders through the system file picker so GlassSSH can access them. If a key or folder has moved, select it again.

This edition does not automatically load your existing `~/.ssh/config` and keeps server trust records in its own app container. A connection that works in Terminal may therefore need its settings entered separately in GlassSSH.

Convert PuTTY `.ppk` keys to OpenSSH format before importing them into the Mac App Store edition.

### Server identity warning

Verify the server fingerprint with your server administrator before accepting it. If a previously trusted server's identity changes unexpectedly, confirm the reason before reconnecting.

### File transfers fail or open in an unexpected folder

- Confirm that your server supports SFTP and that your account has permission to access the destination.
- Make sure the file-transfer panel is associated with the intended active SSH session.
- Following the terminal's current remote directory depends on the remote shell emitting OSC 7 directory updates. If it does not, navigate to the desired folder in the file-transfer panel.
- Transfer activity is shown, but progress is not byte-accurate.

## Keyboard shortcuts

| Action | Shortcut |
| --- | --- |
| Quick Connect | ⌘K |
| New Host | ⇧⌘N |
| Reconnect | ⇧⌘R |
| Duplicate Tab | ⇧⌘D |
| Split Right | ⌘\ |
| Command Palette | ⇧⌘P |

## Privacy when requesting support

GitHub issues and their attachments are public. Never post passwords, private keys, passphrases, access tokens, or other credentials. Review screenshots, logs, and exported profiles before sharing them: even exports without secrets can contain hostnames, usernames, local paths, and details about your infrastructure.

For a suspected security vulnerability, use GitHub's **Report a vulnerability** option under the **Security** tab if it is enabled. Do not disclose sensitive vulnerability details in a public issue.
