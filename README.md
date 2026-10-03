<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/wordmark-white.png">
    <img src="assets/wordmark-black.png" alt="ClipTalk" width="300">
  </picture>
</p>

<h1 align="center">ClipTalk MCP Server</h1>

<p align="center">
  <b>The official Model Context Protocol (MCP) server for ClipTalk: ask your AI assistant for a video and get back a finished, ready-to-post MP4 with script, visuals, voiceover, captions and music, for TikTok, Instagram Reels, YouTube Shorts and YouTube.</b>
</p>

<p align="center">
  <a href="https://github.com/payamsaremi/cliptalk-mcp"><img src="https://img.shields.io/badge/Official-ClipTalk-FF00FF" alt="Official ClipTalk server"></a>
  <a href="server.json"><img src="https://img.shields.io/badge/MCP_Registry-pro.cliptalk%2Fcliptalk-000000?logo=modelcontextprotocol&logoColor=white" alt="MCP Registry: pro.cliptalk/cliptalk"></a>
  <a href="#how-it-works"><img src="https://img.shields.io/badge/Auth-OAuth_2.1-2EBC4F" alt="Auth: OAuth 2.1"></a>
  <a href="#how-it-works"><img src="https://img.shields.io/badge/Transport-Streamable_HTTP-890682" alt="Transport: Streamable HTTP"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/payamsaremi/cliptalk-mcp?label=License&color=FF00FF" alt="License: MIT"></a>
</p>

<p align="center">
  <a href="https://glama.ai/mcp/servers/payamsaremi/cliptalk-mcp"><img src="https://img.shields.io/badge/Glama-listed-000000" alt="Listed on Glama"></a>
  <a href="https://smithery.ai/servers/cliptalkai/cliptalk"><img src="https://img.shields.io/badge/Smithery-listed-EA580C" alt="Listed on Smithery"></a>
  <a href="https://allmcps.com/mcp/cliptalk"><img src="https://allmcps.com/api/badge/cliptalk?style=shield" alt="AllMCPs Verified"></a>
</p>

<p align="center">
  <a href="https://www.cliptalk.pro/mcp"><b>Website</b></a> ·
  <a href="#tools"><b>Tools</b></a> ·
  <a href="#skills"><b>Skills</b></a> ·
  <a href="#data-and-security"><b>Data &amp; security</b></a> ·
  <a href="https://www.cliptalk.pro/contact"><b>Support</b></a>
</p>

---

**ClipTalk** is a hosted MCP server that turns a chat with your AI assistant into a finished video. You describe the video in plain words, ClipTalk writes the script, generates the visuals, adds a voiceover, captions and music, and renders an MP4 you can post straight away. Everything you make lands in your ClipTalk library, so you can keep editing it from the chat or in the ClipTalk editor.

```
https://www.cliptalk.pro/mcp
```

With the ClipTalk MCP server, you can:

* **Make videos from a sentence**: faceless stories, UGC-style product ads, explainers, quizzes, micro-dramas, brainrot shorts and music videos, in vertical, square or horizontal sizes.
* **Remake what works**: paste a link to a video you like and your assistant studies its format and rebuilds it for your brand, or share a product page and turn it into an ad.
* **Edit by asking**: cut silences, fix caption text, change the music or the narrator voice, swap scenes, add motion graphics, change the layout or speed.
* **Bring your own media**: import footage, photos or audio by link, and keep the same presenter character across all your videos.
* **Stay in control of cost**: preview the script and the credit price before anything is made.

Built for content creators, marketers and businesses who already work inside Claude, ChatGPT, Cursor or another MCP client.

## One-click setup

Pick your client. Each button uses the client's native install link, so there is no JSON to edit by hand.

<table align="center">
  <tr>
    <td align="center" width="200">
      <a href="https://cursor.com/en/install-mcp?name=cliptalk&config=eyJ1cmwiOiJodHRwczovL3d3dy5jbGlwdGFsay5wcm8vbWNwIn0%3D">
        <img src="https://img.shields.io/badge/Cursor-000000?style=for-the-badge&logo=cursor&logoColor=white" alt="Add to Cursor"><br>
        <b>Add to Cursor</b>
      </a>
    </td>
    <td align="center" width="200">
      <a href="https://vscode.dev/redirect/mcp/install?name=cliptalk&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fwww.cliptalk.pro%2Fmcp%22%7D">
        <img src="https://img.shields.io/badge/VS_Code-0098FF?style=for-the-badge&logoColor=white" alt="Add to VS Code"><br>
        <b>Add to VS Code</b>
      </a>
    </td>
    <td align="center" width="200">
      <a href="https://insiders.vscode.dev/redirect/mcp/install?name=cliptalk&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fwww.cliptalk.pro%2Fmcp%22%7D&quality=insiders">
        <img src="https://img.shields.io/badge/VS_Code_Insiders-24bfa5?style=for-the-badge&logoColor=white" alt="Add to VS Code Insiders"><br>
        <b>Add to VS Code Insiders</b>
      </a>
    </td>
  </tr>
</table>

### Let your agent do the setup

Most AI coding agents can install and authenticate the server themselves. Paste this prompt into yours:

```
Add the ClipTalk MCP server to this agent. It is a remote Streamable HTTP server at
https://www.cliptalk.pro/mcp with OAuth sign-in (setup guide: https://github.com/payamsaremi/cliptalk-mcp).
Then start the ClipTalk sign-in flow so I can log in.
```

### Add it manually

| Client | Command or configuration |
| --- | --- |
| Claude Code | `claude mcp add --transport http cliptalk https://www.cliptalk.pro/mcp`, then run `/mcp` in a session to sign in |
| Claude Code (plugin, with skills) | `/plugin marketplace add payamsaremi/cliptalk-mcp`, then `/plugin install cliptalk@cliptalk` |
| Claude.ai / Claude Desktop | **Customize → Connectors → Add custom connector**, paste `https://www.cliptalk.pro/mcp`, then sign in. On Team and Enterprise plans an owner adds it once in Organization settings |
| ChatGPT | **Settings → Security and login**, turn on **Developer mode**, then on [chatgpt.com/plugins](https://chatgpt.com/plugins) press **+**, add `https://www.cliptalk.pro/mcp` and sign in |
| Codex CLI | `codex mcp add cliptalk --url https://www.cliptalk.pro/mcp` |
| Gemini CLI | `gemini extensions install https://github.com/payamsaremi/cliptalk-mcp` |
| Cursor | Use the button above, or add `{"mcpServers": {"cliptalk": {"url": "https://www.cliptalk.pro/mcp"}}}` to `~/.cursor/mcp.json` |
| VS Code / GitHub Copilot | Use the button above, or add `{"servers": {"cliptalk": {"type": "http", "url": "https://www.cliptalk.pro/mcp"}}}` to `.vscode/mcp.json` |
| Windsurf | **Cascade → MCP servers → Add custom server**, with `serverUrl` set to `https://www.cliptalk.pro/mcp` |
| Any other MCP client | Add `https://www.cliptalk.pro/mcp` as a Streamable HTTP server; OAuth sign-in starts automatically |

The first time a tool runs, your client opens the ClipTalk sign-in page. Sign in (or create a free account) and press **Allow**.

## Contents

* [One-click setup](#one-click-setup)
* [What you can make](#what-you-can-make)
* [Example prompts](#example-prompts)
* [Tools](#tools)
* [Skills](#skills)
* [How it works](#how-it-works)
* [Credits and pricing](#credits-and-pricing)
* [Data and security](#data-and-security)
* [Troubleshooting](#troubleshooting)
* [Find ClipTalk on](#find-cliptalk-on)
* [Support and feedback](#support-and-feedback)

## What you can make

| Format | What it is |
| --- | --- |
| **Faceless story** | A narrated story over cinematic AI imagery: scary stories, reddit-style confessions, history, true crime, motivational arcs |
| **UGC ad** | A creator talks to camera about your product, UGC style |
| **Explainer** | Narrated motion graphics: animated type, mockups, counters and charts in your brand colors |
| **Quiz** | Quiz and flashcard videos built from motion graphics |
| **Micro-drama** | A scripted scene with characters who speak |
| **Brainrot** | Narration and word-by-word captions over looping satisfying footage or gameplay |
| **Music video** | Shots for your song, timed to the lyrics |
| **Remake** | Study a viral video's format and rebuild it for your brand |
| **Anything else** | Free-form videos scene by scene: your own footage, AI images and clips, talking presenters, motion graphics |

Every video can be vertical (9:16), square (1:1), feed (4:5) or horizontal (16:9), in many languages, with a voice from the voice library.

## Example prompts

* "Make a 30-second video about why octopuses are so smart, with captions and calm music."
* "Here is my product page: https://example.com/product. Turn it into a 20-second TikTok ad."
* "Analyze this viral video and remake it for my bakery: https://www.tiktok.com/@…"
* "Create a presenter character and have her explain our three new features on camera."
* "Make a 5-question quiz video about world capitals."
* "Find an energetic young female voice and use it for my last video."
* "Make that video 1.5x faster, turn off the captions and send me the new link."
* "How many credits would a 60-second video cost? Tell me before you make it."

## Tools

22 tools. Every tool declares MCP annotations: **read-only** tools only look things up; **destructive** tools spend credits (failed generations are refunded) or overwrite an existing video; **open-world** tools may fetch a URL you supply.

### Create

| Tool | What it does | Read-only | Destructive | Open-world |
| --- | --- | :-: | :-: | :-: |
| `list_templates` | List the video formats (faceless story, UGC ad, explainer, quiz…) and what each needs | ✅ | | |
| `plan_from_template` | Dry run: returns the script and the credit price; creates and charges nothing | ✅ | | ✅ |
| `create_from_template` | Make a finished video from a format and a sentence, topic or script | | ✅ | ✅ |
| `create_video` | Make a video scene by scene: your media, AI images and clips, presenters, motion graphics | | ✅ | ✅ |
| `get_motion_dialect` | Reference for writing custom motion-graphics scenes | ✅ | | |

### Follow up and edit

| Tool | What it does | Read-only | Destructive | Open-world |
| --- | --- | :-: | :-: | :-: |
| `list_videos` | List your videos | ✅ | | |
| `get_video` | A video's status and download link | ✅ | | |
| `get_video_assets` | A video's timeline, scenes and assets, ready to edit | ✅ | | |
| `make_contact_sheet` | One image of frames across the whole video, so the assistant can check it | | | |
| `edit_video` | Change captions, music, voice, scenes, layout, speed, trims and silences | | ✅ | ✅ |
| `render_video` | Re-render a video to a new MP4 | | ✅ | |

### Media, voices and characters

| Tool | What it does | Read-only | Destructive | Open-world |
| --- | --- | :-: | :-: | :-: |
| `generate_media` | Generate a single image, clip, voiceover or talking presenter into your library | | ✅ | ✅ |
| `import_media` | Bring in footage, photos or audio from a public link or social post | | | ✅ |
| `upload_media` | Upload a file to your library | | | |
| `list_media` | List your library | ✅ | | |
| `get_media` | One library item's status, link and transcript | ✅ | | |
| `list_voices` | Search the voice library by language, gender, age, accent, tone and use case | ✅ | | |
| `list_music` | List the background music catalog | ✅ | | |
| `list_characters` | List your characters and the public cast of presenters | ✅ | | |
| `create_character` | Save a presenter character (face and voice) to reuse across videos | | ✅ | ✅ |

### Account

| Tool | What it does | Read-only | Destructive | Open-world |
| --- | --- | :-: | :-: | :-: |
| `get_credits` | Your credit balance and plan | ✅ | | |
| `estimate_cost` | Price a request without creating or charging anything | ✅ | | |

## Skills

The [`skills/`](skills/) directory holds one [Agent Skill](https://agent-plugins.org/) per format. Each one tells your assistant what to ask for, when to preview the price, how to wait for the render, and how to check the result before handing it over. The Claude Code, Cursor and Gemini packages in this repo install them together with the server, or add just the skills to any agent:

```bash
npx skills add payamsaremi/cliptalk-mcp
```

| Skill | What it makes | Try |
| --- | --- | --- |
| [`faceless-story`](skills/faceless-story/SKILL.md) | Narrator-led stories over AI visuals | "Make a faceless scary story video" |
| [`ugc-ad`](skills/ugc-ad/SKILL.md) | A creator talks to camera about your product | "Make a UGC ad for my skincare serum" |
| [`explainer-video`](skills/explainer-video/SKILL.md) | Narrated motion-graphics explainer | "Make an explainer video for my app's new feature" |
| [`quiz`](skills/quiz/SKILL.md) | Quiz and flashcard videos in motion graphics | "Make a 5-question quiz video about world capitals" |
| [`micro-drama`](skills/micro-drama/SKILL.md) | A scripted scene with characters who speak | "Make a micro drama about a betrayal caught on camera" |
| [`brainrot`](skills/brainrot/SKILL.md) | Narrated facts and stories over looping footage | "Make a brainrot video about weird space facts" |
| [`music-video`](skills/music-video/SKILL.md) | Shots for your song, timed to the lyrics | "Make a music video for my song" |
| [`remake-viral-video`](skills/remake-viral-video/SKILL.md) | Remake a viral video's format for your brand | "Analyze this viral video and remake it for my brand" |

## How it works

* **Hosted.** ClipTalk runs the server at `https://www.cliptalk.pro/mcp` (Streamable HTTP). There is nothing to install or keep up to date.
* **OAuth 2.1 sign-in.** Authorization code flow with PKCE (S256), dynamic client registration and client ID metadata documents. Your client discovers everything from `/.well-known/oauth-protected-resource` and `/.well-known/oauth-authorization-server`. The assistant gets an access token scoped to your ClipTalk account; it never sees your password.
* **Videos render in the background.** A create or edit call returns a video id right away. The assistant checks `get_video` until the status is `completed` (usually a few minutes), then hands you the MP4 download link.
* **Your library is the source of truth.** Videos, characters and media are saved to your ClipTalk account, so a video made in Claude can be edited later from ChatGPT or in the ClipTalk editor.

## Credits and pricing

Connecting is free, and new accounts start with free credits. Making and editing videos uses credits from your ClipTalk account. `plan_from_template` and `estimate_cost` show the price before anything is made, and failed generations are refunded automatically. Plans and credit packs are at [cliptalk.pro/pricing](https://www.cliptalk.pro/pricing).

## Data and security

* ClipTalk receives only what your assistant sends to its tools: the topic, script, voice or style you ask for, and the links or files you want brought in. It does not receive the rest of your conversation, your other connected apps or your assistant account details.
* Every action runs as your own ClipTalk account. There is no delete tool: the assistant can create and edit videos, but it cannot remove anything from your library.
* Disconnect at any time from your assistant's connector or app settings. Delete videos and media from your library, or ask for account deletion at support@cliptalk.pro.
* Read the full [privacy policy](https://www.cliptalk.pro/privacy-policy) and [terms of use](https://www.cliptalk.pro/terms-of-use). To report a vulnerability, see [SECURITY.md](SECURITY.md).

As with any MCP server, only connect clients you trust, and keep an eye on what your assistant does with tools that spend credits.

## Troubleshooting

| Problem | Fix |
| --- | --- |
| A file attached in the chat doesn't reach ClipTalk | Chat attachments are not passed to MCP servers. Share a link instead, and the assistant will use `import_media` |
| A social video won't import | Private and age-restricted posts can't be imported. Use a public link |
| The video isn't ready yet | Rendering takes a few minutes. Ask the assistant to check on the video again |
| Sign-in loops or fails | Remove the ClipTalk connector from your client and add it again to start a fresh sign-in |
| "Insufficient credits" | Check your balance with `get_credits` and top up at [cliptalk.pro/pricing](https://www.cliptalk.pro/pricing) |

## Find ClipTalk on

ClipTalk is listed in the [official MCP Registry](https://registry.modelcontextprotocol.io/v0/servers?search=pro.cliptalk) (`pro.cliptalk/cliptalk`) and in these directories and marketplaces:

* [Glama](https://glama.ai/mcp/servers/payamsaremi/cliptalk-mcp) and the [Glama connector page](https://glama.ai/mcp/connectors/pro.cliptalk/cliptalk)
* [Smithery](https://smithery.ai/servers/cliptalkai/cliptalk)
* [AllMCPs](https://allmcps.com/mcp/cliptalk)
* [MCPLookup](https://mcplookup.com/server/pro.cliptalk/cliptalk)
* [ClaudeMarketplace](https://www.claudemarketplace.net), the Claude Code plugin and MCP server marketplace
* [agentskill.sh](https://agentskill.sh) for the ClipTalk agent skills

## Support and feedback

* Help and questions: [cliptalk.pro/contact](https://www.cliptalk.pro/contact) or support@cliptalk.pro
* Bugs and feature requests for the MCP server: [open an issue](https://github.com/payamsaremi/cliptalk-mcp/issues)
* Product site: [cliptalk.pro](https://www.cliptalk.pro)

## License

The documentation, client manifests and skills in this repository are released under the [MIT License](LICENSE). The ClipTalk service itself is provided under the ClipTalk [terms of use](https://www.cliptalk.pro/terms-of-use).
