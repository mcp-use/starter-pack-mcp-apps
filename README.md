# Make Something Agents Want: mcp-use Starter Packs

Starter templates for the [Make Something Agents Want Hackathon](https://events.ycombinator.com/MakeSomethingAgentsWant) at Y Combinator HQ in San Francisco, October 17–18, 2026.

YC's motto has always been "make something people want." This weekend the user is an agent. Each starter pack is an MCP server built with [mcp-use](https://github.com/mcp-use/mcp-use), pinned to `mcp-use@2.10.0`, and ready to run, test in the Inspector, and deploy to [Manufact](https://manufact.com).

## Pick a starter pack

| Starter pack | What you get | Start here |
| --- | --- | --- |
| **Blank** | An empty MCP server, straight from `create-mcp-use-app`. Add your own tools, resources, and prompts. | [mcp-use/starter-pack-blank](https://github.com/mcp-use/starter-pack-blank) |
| **MCP Apps** | An MCP server with a React view that renders inside ChatGPT, Claude, and other MCP Apps clients. | [mcp-use/starter-pack-mcp-apps](https://github.com/mcp-use/starter-pack-mcp-apps) |
| **ChatGPT Plugin Extension** | Little Bookshop: a complete ChatGPT app with launchers, native settings, deep links, a cart, and "Add to chat" model context. | [mcp-use/starter-pack-chatgpt-plugin](https://github.com/mcp-use/starter-pack-chatgpt-plugin) |

Open the starter pack you want and click **Use this template** to create your own copy.

## Get started

You need Node.js 22.22.2 or newer.

```bash
git clone https://github.com/<you>/<your-repo>.git
cd <your-repo>
npm install
npm run dev
```

The dev server prints two URLs:

- MCP endpoint: `http://localhost:3000/mcp`
- Inspector: `http://localhost:3000/mcp/inspector`

Open the Inspector to call your tools and preview views. The server reloads when you edit files.

To try your server in ChatGPT or Claude before you deploy, start a public tunnel and add the URL it prints as a connector:

```bash
npm run dev -- --tunnel
```

## Deploy on Manufact

```bash
npx mcp-use login
npm run deploy
```

The first deploy links the project. Your server gets a public HTTPS URL you can add to ChatGPT, Claude, Cursor, or any MCP client. See the [deployment guide](https://docs.mcp-use.com/v2/typescript/server/deployment/mcp-use).

## Manufact track: Best MCP Server for Agents

The best MCP server built for agents as the primary customer.

| Place | Prize |
| --- | --- |
| 1st | $2,000 cash + $6,000 Manufact credits |
| 2nd | $700 cash + $3,000 Manufact credits |
| 3rd | $300 cash + $300 Manufact credits |

Judges: Luigi Pederzani, Enrico Toniato, Andrew Khadder.

Some things that make a server good for agents:

- Tool names and descriptions written for a model to read. Use `.describe()` on every input field.
- Outputs that are small and structured. Return `structuredContent` with an `outputSchema` so agents don't spend tokens parsing prose.
- Errors that tell the agent what to do next, returned as `isError` results instead of thrown stack traces.
- A few well-scoped tools instead of one per API endpoint.

## Schedule

**Saturday, October 17**

| Time | |
| --- | --- |
| 9:00 AM | Doors open and sign in |
| 10:00 AM | Kickoff |
| 10:30 AM | Hacking begins |
| 12:00 PM | Lunch and lightning talks |
| 5:00 PM | Dinner |
| 6:00 PM | Dinner lightning talks |

**Sunday, October 18**

| Time | |
| --- | --- |
| 8:00 AM | Breakfast |
| 10:00 AM | Submissions due and live demos |
| 11:00 AM | Judging completes |
| 12:15 PM | Winners announced |
| 1:00 PM | Hackathon ends |

## Build with a coding agent

Each starter pack ships the `mcp-apps-builder` skill in `.claude/skills`, `.cursor/skills`, and `.agents/skills`. Claude Code, Cursor, Codex, and other agents pick it up automatically and know how to write mcp-use servers and views.

## Resources

- [mcp-use docs](https://docs.mcp-use.com/v2/typescript/getting-started/quickstart)
- [MCP Apps guide](https://docs.mcp-use.com/v2/typescript/mcp-apps)
- [ChatGPT Plugin Extensions guide](https://docs.mcp-use.com/v2/typescript/mcp-apps/chatgpt-extensions)
- [Discord](https://discord.gg/XkNkSkMz3V): ask the Manufact team questions during the hackathon
- [mcp-use on GitHub](https://github.com/mcp-use/mcp-use): star it if these starter packs helped
