# RK Social Automation MCP

**AI-powered Social Media Automation MCP Agent by RK Digital.**

A standalone automation agent designed to manage the social-media lifecycle for multiple clients: brand intelligence, content strategy, AI-assisted content generation, creative planning, approvals, scheduling, publishing adapters, analytics, optimization, and recurring automation.

## Architecture

```text
Client / Business
      |
Brand Intelligence
      |
Strategy Engine
      |
AI Content Engine
      |
Creative Briefs
      |
Approval + Calendar
      |
Scheduler / Automation Worker
      |
Platform Adapter Layer
  |   |   |   |   |   |
 FB  IG  LI  X TikTok YT
      |
Analytics
      |
Optimization
      |
Next Automation Cycle
```

## Nine-phase system

| Phase | Capability |
|---|---|
| 1 | Foundation, MCP server and security |
| 2 | Brand and content intelligence |
| 3 | AI content generation |
| 4 | Creative/media planning |
| 5 | Calendar, approvals and scheduling |
| 6 | Publishing adapter layer |
| 7 | Analytics |
| 8 | Optimization |
| 9 | Autonomous recurring automation |

## Key capabilities

- Multi-client workspaces and client-level data isolation
- Brand voice, audience, pillars, rules, competitors and forbidden topics
- Reusable social strategy generation
- AI-assisted single and batch content generation
- Content quality scoring
- Campaign management and creative briefs
- Draft → approved → scheduled → published workflow
- Facebook, Instagram, LinkedIn, X, TikTok and YouTube adapter boundaries
- Safe dry-run publishing
- Webhook connector bridge for external platform integrations
- Normalized analytics and optimization reports
- Recurring automation rules and worker
- AES-256-GCM encrypted social credentials
- MCP JSON-RPC interface with authentication, permissions, rate limiting and validation
- Atomic local persistence

## Production integration boundary

The agent does **not** invent third-party OAuth credentials. Real publishing requires the relevant official platform app/OAuth configuration. The platform adapter layer is designed so those integrations can be connected without changing the core automation engine.

Use dry-run mode for safe development:

```env
RK_SOCIAL_DRY_RUN=true
```

## Security

Never commit production secrets, OAuth tokens, client data, or `.env` files. Use `.env.example` as the configuration template.

## Local development

Requirements: **Node.js 20+**

```bash
cp .env.example .env
npm test
npm run check
npm start
```

Worker:

```bash
npm run worker
npm run worker:loop
```

## Repository status

The repository contains the complete v2 release archive. The current hardened local build is **v2.0.1**, with additional publishing guards, expired-credential checks, weekly-plan automation coverage, analytics input normalization, and regression tests.

## Project

Built as a dedicated specialist agent within the RK Digital automation ecosystem, alongside separate agents for web development, maintenance, advertising, and future business automation workflows.
