# Credits and third-party notices

This project is a fork of Taskbar AI Usage by Sof2245 that adds the NARIT provider. The
NARIT code in `windhawk-taskbar-ai-narit.wh.cpp` (the `narit` provider, its `/key/info` parser and
its login dialog) is original work of this fork; everything else is the projects below.

All of them are MIT, except Simple Icons, and the MIT text they are distributed under is the one in
[LICENSE](LICENSE).

| Project | Source | Licence | Copyright | Used for |
|---|---|---|---|---|
| Taskbar AI Usage 1.0.2 | https://github.com/Sof2245/taskbar-ai-usage | MIT | (c) 2026 Sof2245 | The mod this project is based on: sign-in, token storage, polling, parsers, settings window, taskbar injection |
| Taskbar AI Quota Bars 1.6.5 | https://github.com/Cleroth/windhawk-taskbar-ai-quota | MIT | (c) Cleroth | The base of Taskbar AI Usage |
| Taskbar Fluent Media Player 1.6.0 | https://github.com/Salyts/Taskbar-Fluent-Media-Player | MIT | (c) 2026 Salyts | Flyout shell, acrylic background, button template and visual-state helpers |
| WinUI (microsoft-ui-xaml) | https://github.com/microsoft/microsoft-ui-xaml | MIT | (c) Microsoft Corporation | Reference only, the `MicaController` effect graph reproduced by the Mica flyout; no code is reused |
| Primer Octicons | https://github.com/primer/octicons | MIT | (c) 2026 GitHub Inc. | The GitHub Copilot logo path, via Simple Icons |
| Simple Icons | https://github.com/simple-icons/simple-icons | CC0-1.0 | public domain | Provider logo paths, except Copilot |

The app logo is this fork's own work.

Claude, Anthropic, OpenAI, Codex, Gemini, Antigravity, GitHub and Copilot are trademarks of their
owners. Their names and logos appear only to identify which account a tile belongs to.

## Antigravity sign-in

The Antigravity flow signs in with a public Google OAuth client that was registered by the
Antigravity integration and is inherited from Taskbar AI Usage. This fork does not own that client
and cannot change or revoke it. A client secret for a desktop app is not treated as confidential by
Google (see [OAuth 2.0 for Mobile and Desktop
Apps](https://developers.google.com/identity/protocols/oauth2/native-app)); the protection is PKCE
plus the loopback redirect, and the secret on its own grants nothing. GitHub secret scanning still
flags it on push, which is expected for this repository. If the owner revokes the client, that one
provider stops working and everything else in the mod keeps working.
