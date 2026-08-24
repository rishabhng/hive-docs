# Hive docs: instructions for agents

## About this project

- Documentation for Hive Intelligence, built on [Mintlify](https://mintlify.com).
- Pages are MDX with YAML frontmatter. Configuration is `docs.json`.
- A new page must be added to `docs.json` navigation or it will not render.
- Published at `docs.hiveintelligence.xyz`. This repository is public: nothing internal,
  no unreleased plans, no internal repository names.

## The product

Hive is **MCP + CLI + Skills**. It is not a REST API product. The HTTP layer still exists as
plumbing for the CLI and dashboard, but it must not be documented as a product surface. If
you find REST described as a way to use Hive, that is stale copy to remove.

## Where facts come from

Every number, endpoint, tool count, provider name, plan limit, and client name traces to
`src/data/mcp-facts.ts` in the private Hive website codebase, or to `src/lib/pricing.ts`
for plan pricing. Do not invent counts and do not round them.

Current values at the time of writing:

- Endpoint `https://mcp.hiveintelligence.xyz/mcp`, plus 10 category endpoints
- 589 provider tools + 18 Hive-native = 607 callable
- 13 providers, 11 documented clients, 17 skill packs
- Hero tools: `get_token_price`, `check_token_safety`, `get_wallet_portfolio`
- Anonymous lane: 25 material calls per IP per day, resetting 00:00 UTC
- CLI `hive-intelligence@1.4.0`

When the product changes, update these docs and this list together.

## Writing rules

- **No em dashes or en dashes.** Use a period, a comma, or restructure the sentence.
- Sentence case headings. Second person. Active voice. One idea per sentence.
- Specific beats vague: "25 material calls per IP per day" not "a generous free tier".
- No rule-of-three cadence, no "not just X, it's Y", no bolded inline-header bullet lists,
  no signposting ("Let's dive in"), no upbeat filler conclusions.
- Bold for UI elements: click **Settings**. Code formatting for files, commands, and paths.
- Say what does not work and where coverage is thin. Honest limits build more trust than
  claims do.

## Content boundaries

- No news, social sentiment, or trend data. Hive deliberately does not serve those.
- No financial advice, price predictions, or buy signals.
- No internal repository names, infrastructure detail, or unreleased roadmap.
