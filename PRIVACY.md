# GlassSSH Privacy Policy

Last updated: September 20, 2026

This policy explains how GlassSSH handles information when you use the macOS app and its GitHub support repository.

## Overview

GlassSSH is an SSH client that connects to servers you choose. It does not require an account with the developer and does not include advertising, tracking, or analytics services. The app does not send your connection profiles, credentials, or terminal content to the developer.

## Information stored on your Mac

GlassSSH stores information locally to provide its features:

- **Connection profiles:** server addresses, ports, usernames, groups, tags, favorites, authentication settings, private-key file paths, jump hosts, and tunnel settings.
- **Session settings:** terminal preferences, working directories, startup commands, configured environment variables, and the time of the last connection.
- **Saved credentials:** passwords and key passphrases you explicitly choose to save are stored in Apple Keychain, separately from connection profiles. These Keychain items are configured to be accessible only while your device is unlocked and to remain specific to that device.
- **File access permissions:** the sandboxed edition stores permission bookmarks for files and folders you select so it can access them again after restarting.
- **Server trust records:** OpenSSH stores known server identities for host-key verification. The sandboxed Mac App Store edition uses its own app container; other builds may use your existing OpenSSH files.

Private keys remain in the files you select. GlassSSH reads them as needed for authentication and does not upload their contents to the developer.

## Connections, terminal sessions, and file transfers

When you connect, authentication and session traffic is exchanged with the SSH server you select and any jump hosts you configure. Commands and terminal input are sent to the remote server, and the app displays the server's responses.

SFTP uploads and downloads transfer the files you select between your Mac and the remote server. SSH tunnels carry traffic to destinations determined by your forwarding settings and the applications using those tunnels.

SSH encrypts the connection between SSH endpoints. Traffic beyond a tunnel's remote endpoint depends on the protocol used for that traffic. Remote servers, jump hosts, and destination services may process or log your IP address, account information, commands, files, or other activity according to their own policies. GlassSSH does not control those systems.

## Importing and exporting profiles

Profile imports are processed on your Mac. JSON exports are saved to the location you choose and do not include passwords or passphrases stored in Keychain, or private-key file contents.

Exports do include connection settings, which can contain sensitive information such as hostnames, usernames, file paths, environment variables, and startup commands. Any secrets you manually place in those settings may also appear in an export. Review exported files before sharing them.

## Support requests

Information you voluntarily submit through GitHub, such as issue descriptions, screenshots, and diagnostic details, is available to the repository maintainers and is used to investigate and respond to your request. Public issues and attachments are also visible to other people.

Do not post passwords, private keys, passphrases, access tokens, or confidential terminal output. Remove sensitive details from screenshots, logs, and exported profiles before sharing them. GitHub processes information submitted to its service under its own privacy policy.

## Apple and other services

Apple may separately process App Store purchase information and diagnostic information according to your settings and Apple's policies. This is separate from the app's own handling of data.

If you open an external web link, your browser and the destination website handle that visit under their own settings and policies.

## Retention and deletion

Saved profiles and preferences remain on your Mac until you remove them or the app's local data. You can delete saved hosts in GlassSSH; deleting a host also requests deletion of its associated saved password and passphrase from Keychain.

Uninstalling the app does not necessarily remove its local data or Keychain items. These may need to be removed separately using macOS tools. Selected private-key files, downloaded files, exported profiles, and backups remain wherever you saved them until you delete them separately.

Deleting local app data does not delete files or logs on remote servers, or information you have posted to GitHub. Those copies are managed by the relevant service or administrator.

## Changes to this policy

Updates to this policy will be published in this file with a revised “Last updated” date.

## Privacy questions

For general privacy questions, open an issue in this support repository. Keep public questions free of personal, confidential, or security-sensitive information.
