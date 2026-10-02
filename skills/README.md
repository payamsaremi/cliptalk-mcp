# ClipTalk skills

One [Agent Skill](https://agent-plugins.org/) per video format, each at `skills/<name>/SKILL.md`. They target the ClipTalk MCP server at `https://www.cliptalk.pro/mcp` and are what the Claude Code, Cursor and Gemini packages in this repo install.

Each skill tells the assistant what to ask the user for (and nothing more), when to preview the script and price with `plan_from_template`, how to wait for the render with `get_video`, how to check the frames with `make_contact_sheet`, and how to hand over the download link. `agents/openai.yaml` holds the ChatGPT display metadata for the same skill.
