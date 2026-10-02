# Security policy

Thanks for helping keep the ClipTalk MCP server and the people who use it safe.

## Reporting a vulnerability

**Please don't open a public GitHub issue for a security problem.** Public issues are visible to everyone and can put users at risk before a fix is ready.

Email **support@cliptalk.pro** with the subject line "Security" instead. A good report usually includes:

- What you found, and why you think it's a security issue
- Steps to reproduce, or a proof of concept
- The affected component (a file in this repo, a client manifest, or the hosted endpoint)
- The impact you think it could have

## What this repository covers

This repo holds the public pieces of the ClipTalk MCP server: the documentation, the client manifests (`.mcp.json`, `mcp.json`, and the Claude, Cursor and Gemini plugin manifests), the MCP Registry entry (`server.json`), and the [skills](skills/).

The server itself is a hosted service at `https://www.cliptalk.pro/mcp`. Issues in the hosted service or in sign-in go through the same email above. ClipTalk maintains and updates the hosted server, so there's nothing for you to patch on your end.

## Using the MCP server safely

MCP lets an AI agent act in your ClipTalk account with your permissions, including tools that spend credits. Language models can be tricked by [prompt injection](https://owasp.org/www-community/attacks/PromptInjection), where hidden instructions in a web page or file push an agent to do things you never asked for.

A few habits that lower the risk:

- Connect only MCP clients you trust.
- Ask your assistant to show the price (`plan_from_template` or `estimate_cost`) before it makes anything large.
- Disconnect ClipTalk from clients you no longer use.

## Coordinated disclosure

Please give us a fair chance to investigate and ship a fix before you share details publicly.
