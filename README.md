# Canva MCP Alternatives: 7 Design MCP Servers for Claude (2026)

This list tracks 7 alternatives to the Canva MCP server, checked against vendor pages and Anthropic's connector directory in October 2026. They are ranked by whether an agent can make or change on-brand designs and images through MCP. Wireflow is first because a connected agent can build, run and schedule a whole image or video workflow. Of the 7, 2 are listed in Anthropic's connector directory, as Canva is.

1. **Wireflow**: Best overall for generating on-brand images and video from an agent, a node canvas with an MCP connector and a REST API
2. **Adobe for Claude**: Best for editing photos, video and designs with Adobe apps from Claude, a directory-listed connector with 67 tools
3. **Figma**: Best for agents that read and write Figma files, a remote MCP server with design context and image tools
4. **Bannerbear**: Best for images and videos rendered from branded templates, an API and MCP for template rendering
5. **Placid**: Best for branded visuals filled from data, a template toolkit with REST APIs and an MCP
6. **Orshot**: Best for bulk renders from spreadsheet rows, a template API with an MCP server and a free plan
7. **Cloudinary**: Best for managing and transforming media assets from an agent, a media platform with five MCP servers

The Wireflow team maintains this list, so read entry 1 with that in mind. [Wireflow's AI workflow builder page](https://www.wireflow.ai/ai-workflow-builder) describes the canvas that entry 1 refers to. Every other entry links to the vendor's own pages, so each cell can be checked.

The tables below are generated from [`data/tools.json`](data/tools.json) by [`scripts/update.js`](scripts/update.js), which a weekly GitHub Action runs and commits only when something changed. Every tool on this list is a hosted product with no first-party open-source repo, so there are no star counts to report. The refresh re-stamps the check date and regenerates the tables from the data.

<!-- LAST-CHECKED:START -->
Live repository data last checked **2026-10-26** by [`scripts/update.js`](scripts/update.js), which runs weekly via GitHub Actions.
<!-- LAST-CHECKED:END -->

Maintained by [a1adams](https://github.com/a1adams). Corrections are welcome, see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [The data](#the-data)
- [Capability scores](#capability-scores)
- [Comparison table](#comparison-table)
- [The tools](#the-tools)
  - [Wireflow](#1-wireflow)
  - [Adobe for Claude](#2-adobe-for-claude)
  - [Figma](#3-figma)
  - [Bannerbear](#4-bannerbear)
  - [Placid](#5-placid)
  - [Orshot](#6-orshot)
  - [Cloudinary](#7-cloudinary)
- [Canva, the baseline](#canva-the-baseline)
- [What each check means](#what-each-check-means)
- [How this list is maintained](#how-this-list-is-maintained)
- [FAQ](#faq)
- [Contributing](#contributing)
- [License](#license)

## The data

One row per tool, one column per thing people actually check before committing. Columns with nothing verified behind them are dropped rather than filled with guesses.

<!-- DATA-TABLE:START -->
| Tool | Claude connection | REST API | Free tier | Model support | Pricing |
|---|---|---|---|---|---|
| **[Wireflow](#1-wireflow)** | Custom connector, OAuth sign-in | Yes | [check](https://www.wireflow.ai/pricing) | 100+ image, video and audio models as nodes | [pricing](https://www.wireflow.ai/pricing) |
| **[Adobe for Claude](#2-adobe-for-claude)** | Directory connector, 67 tools | n/a | n/a | n/a | n/a |
| **[Figma](#3-figma)** | Directory connector, remote MCP | n/a | Yes | n/a | [pricing](https://www.figma.com/pricing) |
| **[Bannerbear](#4-bannerbear)** | MCP connection | Yes | [check](https://www.bannerbear.com/pricing/) | n/a | [pricing](https://www.bannerbear.com/pricing/) |
| **[Placid](#5-placid)** | MCP for templates | Yes | [check](https://placid.app/pricing) | n/a | [pricing](https://placid.app/pricing) |
| **[Orshot](#6-orshot)** | MCP server | Yes | Yes | n/a | [pricing](https://orshot.com/pricing) |
| **[Cloudinary](#7-cloudinary)** | Five remote MCP servers, OAuth | Yes | Yes | n/a | [pricing](https://cloudinary.com/pricing) |
<!-- DATA-TABLE:END -->

## Capability scores

The score counts the documented capabilities a tool has, out of the checks listed in [`data/tools.json`](data/tools.json) under `capabilityChecks`. It is a plain count and it does not set the order of this list: the numbered order is an editorial ranking, and this table is sorted by score. The checks and every answer are in the file, so each cell can be checked. Disagree with a cell? Open an issue naming the tool, the check and the evidence.

<!-- CAPABILITY-SCORES:START -->
| Tool | MCP server | Listed in Anthropic's directory | Generates images | Edits existing designs | Fills templates with data | Batch in one call | Free plan | Score |
|------|---|---|---|---|---|---|---|-------|
| **[Adobe for Claude](#2-adobe-for-claude)** | ✅ | ✅ | ✅ | ✅ | n/a | ✅ | ✅ | **6/7** |
| **[Figma](#3-figma)** | ✅ | ✅ | ✅ | ✅ | n/a | ✅ | ✅ | **6/7** |
| **[Wireflow](#1-wireflow)** | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ | n/a | **5/7** |
| **[Bannerbear](#4-bannerbear)** | ✅ | n/a | ✅ | n/a | ✅ | ✅ | n/a | **4/7** |
| **[Orshot](#6-orshot)** | ✅ | n/a | ✅ | n/a | ✅ | n/a | ✅ | **4/7** |
| **[Cloudinary](#7-cloudinary)** | ✅ | n/a | ✅ | ✅ | n/a | n/a | ✅ | **4/7** |
| **[Placid](#5-placid)** | ✅ | n/a | ✅ | n/a | ✅ | n/a | n/a | **3/7** |
<!-- CAPABILITY-SCORES:END -->

## Comparison table

| Tool | Best for | Pricing basis | What an agent can do | Sign-in |
|---|---|---|---|---|
| **Wireflow** | Generating on-brand images and video | Credits per generation | Build, run and schedule workflows | OAuth, no API key |
| **Adobe for Claude** | Editing with Adobe apps from Claude | Not published for the connector | Edit photos, video and designs | Optional, more when signed in |
| **Figma** | Agents working on Figma files | Seats, Full seat $16 a month | Write to the canvas on a Full seat | Figma account |
| **Bannerbear** | Images and videos from templates | Credits, from $49 a month | Create templates, render images | Not published |
| **Placid** | Branded visuals from templates | Credits, from $19 a month | Connect agents to templates | Not published |
| **Orshot** | Bulk renders from sheet rows | Credits, Free has 100 a month | Render from your templates | Not published |
| **Cloudinary** | Media assets and transformations | Credits, Free has 25 a month | Upload, transform, generate | OAuth by default |

From each vendor's own pages and Anthropic's connector directory, checked 2026-10-11. Prices change, so follow the pricing links in the data table.

## The tools

### 1. Wireflow

*Best overall for generating on-brand images and video from an agent*

![Wireflow screenshot](https://assets.wireflow.ai/competitors/wireflow-70f47ccd9660.png?v=r5)

- **What it is:** [Wireflow](https://www.wireflow.ai/) is a hosted platform where ad teams and AI agents build and rerun creative on a shared node board. Each model is a node on one canvas. The output of one node feeds the next.
- **Best for:** Teams that want Claude to make new on-brand images and video, not only fill a design template.
- **Pricing basis:** Credits per generation, according to the model you run. 1 credit is US$0.01, and Starter is US$24 a month with 1,600 credits. Connecting is free, and so is everything the agent reads. See the [Wireflow pricing page](https://www.wireflow.ai/pricing), checked October 2026.
- **Standout:** Through the connector an agent can browse and clone templates, build a workflow from a description, edit node settings, run it and read back the results. It can also put a workflow on a repeating schedule. Source: [the Wireflow MCP page](https://www.wireflow.ai/mcp).
- **Limit:** Wireflow is not listed in Anthropic's connector directory: you add `https://www.wireflow.ai/api/mcp` as a custom connector. Creating, editing and deleting workflows are opt-in permissions, and deleting a workflow through a connector has no undo. Running generations needs a paid plan.
- **API or automation:** A second connector, the Wireflow Editor connector, reads, edits and renders video timelines and image composites, and it does not generate images, video or audio. A composite renders at up to 4096 x 4096, as [the Editor connector reference](https://www.wireflow.ai/docs/mcp/editor) states.
- **Note:** Not listed in Anthropic's connector directory; added as a custom connector by URL (checked 2026-10-11).
- **Sources:** the Wireflow homepage, pricing page, MCP page, MCP reference and Editor connector reference, checked 2026-10-11.
- **Links:**
  - [Wireflow AI workflow builder page](https://www.wireflow.ai/ai-workflow-builder)
  - [Docs](https://www.wireflow.ai/docs/api/overview)

Any client that speaks MCP over Streamable HTTP can connect, and the MCP page has setup steps for Claude, Claude Code, Cursor, ChatGPT and Grok. Brand kits are saved as named assets, and a connected agent can list them by kind or keyword. Pick Wireflow when the agent has to create the imagery itself. Wireflow also has an [AI brand kit generator](https://www.wireflow.ai/features/ai-brand-kit-generator).

Add the Wireflow connector to Claude Code, from the wireflowINC/skills README. Then run /mcp to sign in.
```bash
claude mcp add --transport http wireflow https://www.wireflow.ai/api/mcp
```

### 2. Adobe for Claude

*Best for editing photos, video and designs with Adobe apps from Claude*

![Adobe for Claude screenshot](https://assets.wireflow.ai/competitors/adobe-for-claude-f74300f6dc39.png?v=r5)

- **What it is:** [Adobe for Claude](https://www.adobe.com/adobe-connectors/adobe-for-claude.html) brings Adobe Express, Acrobat, Photoshop, Lightroom, Illustrator, Firefly, Premiere, InDesign and Adobe Stock tools into a Claude conversation.
- **Best for:** People who already use Adobe apps and want to edit images, video, designs and documents by describing the change in Claude.
- **Pricing basis:** Not published for the connector. Many tools work without signing in, a free Adobe account unlocks more, and some tools need an eligible paid Adobe plan.
- **Standout:** Anthropic's connector directory lists it as made by Adobe Inc., with the connector URL `https://adobe-creativity.adobe.io/mcp` and 67 tools. Photos can be edited one at a time or in bulk. Source: [the Adobe listing in Anthropic's connector directory](https://claude.com/marketplace/connectors/adobe-creativity).
- **Limit:** It does not include every feature from each Adobe app. Layer and mask control and opening a layered PSD file are not described, and team or admin controls are not described.
- **Output:** Edited photos, resized images and video for several platforms, designs with personalised text and replaced images, and studio-quality scenes. When you are signed in, supported work is saved to Creative Cloud.
- **Note:** Many tools work without signing in; some need an eligible paid Adobe plan (checked 2026-10-11).
- **Sources:** the Adobe for Claude page and the directory listing linked in this entry, checked 2026-10-11.

Adobe for Claude is the closest match to the Canva connector for editing existing designs inside a chat. It runs in Claude on web and desktop and in Claude Code.

The Adobe connector URL, from the Adobe listing in Anthropic's connector directory. Adobe's own setup is to add Adobe for Claude from Plugins in Claude, connect it on the Connectors tab, then type /adobe in a new conversation.
```text
https://adobe-creativity.adobe.io/mcp
```

### 3. Figma

*Best for agents that read and write Figma files*

![Figma screenshot](https://assets.wireflow.ai/competitors/figma-0b28f0783337.png?v=r5)

- **What it is:** [Figma](https://www.figma.com/) is a design platform, and its Weave product offers AI workflows for imagery, video and audio.
- **Best for:** Design teams that already work in Figma and want agent access to design context and AI images.
- **Pricing basis:** Seats on Professional: a Collab seat is $3 a month, a Dev seat $12 and a Full seat $16. The Starter plan is free with limited access. See the [Figma pricing page](https://www.figma.com/pricing), checked October 2026.
- **Standout:** The `use_figma` tool creates, edits, deletes and inspects objects in Figma Design files, FigJam boards and Figma Slides, and `generate_image` makes a raster image from a prompt with Figma AI credits. Source: [Figma's MCP tools reference](https://developers.figma.com/docs/figma-mcp-server/tools-and-prompts/).
- **Limit:** Writing to files needs a Full seat and edit permission, and Dev seats are read-only. View and Collab seats get up to 20 tool calls a month, and Dev and Full seats up to 200 a day on Professional. The image from `generate_image` is not placed on the canvas.
- **Output:** Design changes in your files, exported PNG, JPG, SVG or PDF assets for up to 20 nodes per call, and runs of published Weave workflows. Claude Code adds the remote server with `claude mcp add --transport http figma https://mcp.figma.com/mcp`, as [Figma's remote server guide](https://developers.figma.com/docs/figma-mcp-server/remote-server-installation/) shows.
- **Note:** Writing to files through MCP needs a Full seat and edit permission; Dev seats are read-only (checked 2026-10-11).
- **Sources:** the Figma pricing page, MCP tools reference, remote server guide and [rate limits page](https://developers.figma.com/docs/figma-mcp-server/rate-limits-access/), checked 2026-10-11.

Figma fits a team whose designs already live in Figma files. Anthropic's directory lists Figma with 9 tools, and `use_figma` is not among them.

Add Figma's remote MCP server to Claude Code, from Figma's remote server installation guide.
```bash
claude mcp add --transport http figma https://mcp.figma.com/mcp
```

### 4. Bannerbear

*Best for images and videos rendered from branded templates*

![Bannerbear screenshot](https://assets.wireflow.ai/competitors/bannerbear-3fd59f0f16df.png?v=r5)

- **What it is:** [Bannerbear](https://www.bannerbear.com/) is an API and no-code platform for generating images, videos and PDFs at scale from templates.
- **Best for:** Teams that need many template-based images or videos from data or code.
- **Pricing basis:** Credits. Automate is $49 a month with 1,000 API credits and 200 AI credits, Scale is from $149 a month and Enterprise from $299. A free trial has 30 API credits with no card. See the [Bannerbear pricing page](https://www.bannerbear.com/pricing/), checked October 2026.
- **Standout:** Its MCP connection lets an assistant such as Claude, ChatGPT or Codex create templates, generate images and run workflows. Workflows chain renders and video tools into one multi-step process run with a single call.
- **Limit:** Requests are refused when credits run out, and trial accounts are limited to three image templates, three animation templates and three workflows. Renders are charged when they are created, so a render that fails after that point is already counted.
- **Output:** Images, videos and PDFs from branded templates. The Image API can batch up to 100 renders in a single call, as [Bannerbear's developer docs](https://developers.bannerbear.com/) describe.
- **Note:** The free trial has 30 API credits and no card. A trial is not listed here as a free tier.
- **Sources:** the Bannerbear pricing page and developer docs linked in this entry, checked 2026-10-11.

Bannerbear fits a team that already has its designs as templates and wants an agent to fill them. Editing a free-form design is not described: the work starts from a template and data.

### 5. Placid

*Best for branded visuals filled from data*

![Placid screenshot](https://assets.wireflow.ai/competitors/placid-1068128ebdaa.png?v=r5)

- **What it is:** [Placid](https://placid.app/) is a creative automation toolkit that generates images, PDFs and videos from templates.
- **Best for:** Teams producing branded visuals at scale from templates and data.
- **Pricing basis:** Credits. Basic is $19 a month with 500 credits, Pro $39 with 2,500, Business $89 with 25,000 and VIP $249 with 100,000. One image costs 1 credit, and previews are free and watermarked in test mode. See the [Placid pricing page](https://placid.app/pricing), checked October 2026.
- **Standout:** It offers Image, PDF and Video Automation REST APIs and an MCP for connecting agents to templates. Placid Studio lets a team generate branded visuals by filling out a shareable form with live previews.
- **Limit:** There are no overage fees: when the credits run out you cannot generate until you upgrade. A native Google Sheets or CSV import is not named, and a review or approval step is not described.
- **Output:** Images, PDFs and videos. Template placeholders take text, photos or videos, and dynamic elements resize to fit, as [Placid's dynamic templates page](https://placid.app/product/dynamic-templates) explains.
- **Note:** The free trial has a few complimentary credits and no card. A trial is not listed here as a free tier.
- **Sources:** the Placid pricing page, dynamic templates page and [Placid's REST API reference](https://placid.app/docs/2.0/rest/images), checked 2026-10-11.

Placid fits a team that wants agents and non-designers to fill the same templates. Unused credits roll over up to double the monthly amount.

### 6. Orshot

*Best for bulk renders from spreadsheet rows*

![Orshot screenshot](https://assets.wireflow.ai/competitors/orshot-8ac0e8dde45a.png?v=r5)

- **What it is:** [Orshot](https://orshot.com/) is an API that generates images, PDFs and videos from your templates.
- **Best for:** Teams rendering bulk images from spreadsheet rows or automations.
- **Pricing basis:** Credits. 1 credit is 1 image, 1 PDF page or 1 second of video. Free has 100 credits a month with no card, and Launch is $39 a month with 1,500 credits. See the [Orshot pricing page](https://orshot.com/pricing), checked October 2026.
- **Standout:** Orshot Workflows render one image or PDF per row from Google Sheets, Airtable, a CSV or a webhook payload, and can write the render URL back to your sheet. It has an MCP server for Claude, ChatGPT and Cursor.
- **Limit:** Free has 1 workspace, 1 team member and no video, and unused credits do not roll over. Orshot's own image API page says it is not the right fit for one-off art or photos that no template covers.
- **Output:** PNG, JPG or WebP images, PDFs and videos from templates. The render endpoint is `POST /v1/studio/render`, and official SDKs exist for Node.js, Python, PHP and Ruby, as [Orshot's docs index](https://orshot.com/llms.txt) lists.
- **Sources:** the Orshot pricing page, docs index and [Orshot's workflow builder page](https://orshot.com/features/workflow-automation-builder), checked 2026-10-11.

Orshot fits a team whose data already sits in a sheet and whose designs are templates. It is the only template tool on this list with a free monthly plan.

### 7. Cloudinary

*Best for managing and transforming media assets from an agent*

![Cloudinary screenshot](https://assets.wireflow.ai/competitors/cloudinary-837fad2c3430.png?v=r5)

- **What it is:** [Cloudinary](https://cloudinary.com/) is a media platform for uploading, transforming, storing and delivering images and video through an API and CDN.
- **Best for:** Developers and teams that need to resize, optimise and serve media assets at scale.
- **Pricing basis:** Credits. Free is $0 with 25 monthly credits and 3 users, and includes API and MCP server access. Plus is $89 a month billed yearly ($99 billed monthly) with 225 credits. See the [Cloudinary pricing page](https://cloudinary.com/pricing), checked October 2026.
- **Standout:** Cloudinary runs five MCP servers: Asset Management, Environment Config, Structured Metadata, Analysis and MediaFlows. The remote servers use OAuth by default, with API keys in headers as an option. Source: [Cloudinary's MCP docs](https://cloudinary.com/documentation/cloudinary_llm_mcp).
- **Limit:** The free plan is capped at 25 monthly credits and 3 users. Image generation from a prompt needs the Image Generation add-on.
- **Output:** Uploaded, searched, renamed and transformed assets, transformation URLs, and images generated from a prompt or reference images with the add-on. The Cloudinary plugin for Claude installs selected Cloudinary Skills plus all the remote MCP servers.
- **Note:** Image generation through the Asset Management MCP server needs the Image Generation add-on (checked 2026-10-11).
- **Sources:** the Cloudinary pricing page and MCP docs linked in this entry, checked 2026-10-11.

Cloudinary fits a team whose assets already live in Cloudinary and who want an agent to manage them. It is a media pipeline, not a design editor.

## Canva, the baseline

Canva's own connector is the product this list is measured against, so it is described here and not ranked. These lines come from Canva's pricing page and Anthropic's connector directory, checked 2026-10-11.

- **What it is:** Canva is an online design platform with templates, brand kits and built-in AI tools. Its connector works with Claude and is available on all Canva accounts.
- **Directory listing:** Anthropic's connector directory lists Canva as Anthropic verified and made by Canva, with sign-in required and the connector URL `https://mcp.canva.com/mcp`.
- **Tools:** 17 tools that search, read, import, generate and export designs, organise folders and add a comment thread to a design. They include generate-design, import-design-from-url, export-design and get-export-formats.
- **Plans:** a Free plan at US$0 with up to 20 Standard or Premium AI uses a month and 1 brand kit, and Pro at US$144 a year for one person.
- **Where it stops:** a tool that edits a layer, a mask or a text box inside an existing design is not among the 17 tools, and some actions such as Brand Template search need a paid plan.

## What each check means

A check means the vendor's own page documents it. A cross means the page says it works another way. Anything in brackets is not published, or not verified for this list. That is not proof that it is absent.

- **MCP server:** A documented Model Context Protocol server that Claude can connect to.
- **Listed in Anthropic's directory:** The connector appears in Anthropic's connector directory.
- **Generates images:** An agent can produce a new image through the server.
- **Edits existing designs:** An agent can change an existing design, file or image.
- **Fills templates with data:** A saved template is filled with text, images or rows of data.
- **Batch in one call:** One request covers many outputs.
- **Free plan:** A free plan or free use that covers the MCP server.

## How this list is maintained

Every cell comes from the vendor's own pricing page, MCP docs or product pages, or from Anthropic's connector directory, last checked on 11 October 2026. The numbered order is editorial and uses 4 checks: whether an agent can make or change on-brand designs and images through MCP, whether the product can be bought today without a sales call, how complete the MCP documentation is, and whether the server is listed in Anthropic's directory. The capability score in the README is a plain count of documented checks, and it does not set the order. Nothing here was benchmarked, so no design was made through any of these servers for this list.

The list is capped at 7 servers that make or change images and designs, not general file or productivity servers. To correct a cell, open an issue or a pull request with the tool, the check and a link to the vendor page that proves it. PRs are welcome, including corrections to entry 1. A guide to [automating brand content creation with AI](https://www.wireflow.ai/blog/how-to-automate-brand-content-creation-with-ai) is on the Wireflow blog.

- [`data/tools.json`](data/tools.json) is the source of truth. The tables in this README are generated from it and are overwritten on every run, so edit the JSON, not the tables.
- [`scripts/update.js`](scripts/update.js) fetches star counts and latest release tags from the GitHub API for the tools that publish an official repo, stamps the check date, and regenerates the tables. `--offline` regenerates without the network; `--check` exits non-zero if the README has drifted from the data.
- [`.github/workflows/refresh.yml`](.github/workflows/refresh.yml) runs it weekly and on manual dispatch, and commits only when the data actually changed.
- Prices are deliberately not stored as numbers. A stale price in a comparison table is worse than no price, so the table links to each vendor's own pricing page.

## FAQ

<details>
<summary><strong>What is the Canva MCP server?</strong></summary>

It is Canva's own connector for AI assistants. Anthropic's directory lists it as made by Canva, at `https://mcp.canva.com/mcp`, with 17 tools that search, read, import, generate and export designs. It works with Claude and is available on all Canva accounts.

</details>

<details>
<summary><strong>Is there an official Canva MCP server?</strong></summary>

Yes. Anthropic's connector directory lists the Canva connector as Anthropic verified and made by Canva, checked on 11 October 2026. Sign-in to a Canva account is required, and some actions, such as Brand Template search, need a paid plan.

</details>

<details>
<summary><strong>How do I connect Canva to Claude?</strong></summary>

Canva's connector is listed in Anthropic's connector directory with the URL `https://mcp.canva.com/mcp`, and sign-in to a Canva account is required. Of the alternatives here, Adobe for Claude and Figma are in the same directory, and Wireflow is added as a custom connector by URL.

</details>

<details>
<summary><strong>What is Figma MCP?</strong></summary>

It is Figma's MCP server. It gives an agent design context from Figma files, and on a Full seat its `use_figma` tool creates and edits objects in the file. Claude Code adds the remote server with one `claude mcp add` command.

</details>

<details>
<summary><strong>Is there a Photoshop MCP?</strong></summary>

Adobe for Claude includes Photoshop tools alongside Express, Lightroom, Illustrator, Firefly and others, in one connector with 67 tools. Layer and mask control and opening a layered PSD file are not described on Adobe's page.

</details>

<details>
<summary><strong>Can an agent make many designs in one request?</strong></summary>

Yes, on some servers. Bannerbear batches up to 100 renders in a single call, Figma's Weave tool starts 1 to 10 runs at once, and Wireflow's Compositor renders up to 50 rows per batch from one layout, as [Wireflow's batch guide](https://www.wireflow.ai/docs/batch-image-generation) explains.

</details>

## The short version

Pick Wireflow when the agent has to generate new on-brand images or video, not only fill a template. Pick Adobe for Claude when the work is editing existing photos and designs with Adobe tools, and Figma when the designs live in Figma files. Pick Bannerbear, Placid or Orshot when your designs are templates and the job is filling them from data. Before you switch, run the same five requests through your two finalists and note what each one could not do. To start from a working board, browse [Wireflow's blueprint library](https://www.wireflow.ai/blueprints).

## Contributing

Corrections and additions are welcome, including corrections to the entry for the tool that maintains this list. Open an issue with the tool name, a working link, one line on what it does that the tools already listed do not, and one line on where it stops. Entries are judged on whether they are usable today, not on popularity. Full rules in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC0 1.0 Universal](LICENSE), public domain. Take the data, fork the list, no attribution required.

---

Maintained by [a1adams](https://github.com/a1adams).
