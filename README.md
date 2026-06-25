# Codex Skills — Professional AI System Prompts

> **Turn OpenAI Codex/GPT into a Principal-level Software Engineer.**

Production-grade system prompts that transform OpenAI's Codex and GPT models into a senior/staff/principal engineer with deep expertise across frontend and backend engineering. Every prompt is meticulously crafted to enforce best practices, eliminate lazy patterns, and ensure output that is secure, performant, accessible, and maintainable.

---

## Why Codex-Specific?

OpenAI's Codex and GPT models have unique strengths — exceptional code generation, long context handling, function calling support, and iterative refinement capabilities. These prompts leverage those strengths while adding strict engineering discipline. Each prompt includes **OpenAI-specific behavioral guidance** (Section 18 in frontend, Section 16 in backend) covering precision coding, code-first output, iteration patterns, function calling compatibility, and embedded safety practices.

---

## Available Skill Prompts

| Prompt | Role | Coverage |
|--------|------|----------|
| [`frontend-skills.md`](./frontend-skills.md) | Principal Frontend Engineer | HTML5 semantics, CSS3 deep fundamentals, TypeScript strict, React 19 hooks, Next.js App Router, state management, Core Web Vitals, WCAG 2.2 AA, testing (unit to E2E), security (CSP, XSS, CSRF), PWA, i18n, design systems, form handling, real-time patterns, CI/CD |
| [`backend-skills.md`](./backend-skills.md) | Principal Backend Engineer | PHP/Laravel 11+, Node.js/TypeScript (Express, Fastify, NestJS, Hono), Python (Django, FastAPI), Go, PostgreSQL/MySQL indexing, Redis, MongoDB, REST/GraphQL/gRPC, auth (JWT, OAuth2, Passkeys, RBAC/ABAC/ReBAC), Clean/CQRS/Event-Driven architecture, caching, queues, OWASP Top 10, DevOps (Docker, CI/CD, Terraform), testing |

---

## How to Use

### Option 1: Cursor / Windsurf / Cline Custom Instructions

Copy the contents of the skill file into your AI coding tool's system prompt or custom instructions field.

**With Cline:** Place the `.md` file in your project and reference it via `.clinerules`.

### Option 2: Direct Prompt Injection

Paste the entire skill prompt at the beginning of your conversation with ChatGPT, GPT-4, or any OpenAI model:

```
[Paste frontend-skills.md or backend-skills.md content here]

---

Now, [your task here]
```

### Option 3: OpenAI API System Message (Recommended)

Use the skill prompt as the `system` message in the OpenAI API:

```javascript
const response = await openai.chat.completions.create({
  model: "gpt-4o",
  messages: [
    { role: "system", content: frontendSkillsPrompt },
    { role: "user", content: "Build me a checkout form with..." }
  ]
});
```

### Option 4: Custom GPTs

Create a custom GPT with the skill prompt as its instructions:
1. Go to ChatGPT → Explore GPTs → Create
2. Paste the skill prompt into the "Instructions" field
3. Configure name, description, and capabilities
4. Use your custom Principal Frontend/Backend Engineer GPT for all coding tasks

### Option 5: GitHub Copilot / Custom Instructions

Add the content to your IDE's custom instructions/rules file. For VS Code with GitHub Copilot, add to `.github/copilot-instructions.md`.

---

## What Makes These Different?

| Trait | Default AI Code | With These Prompts |
|-------|----------------|-------------------|
| **Error handling** | Often missing | Every state handled (loading, empty, error, edge cases) |
| **Accessibility** | Usually ignored | WCAG 2.2 AA built-in, keyboard nav, screen reader tested |
| **Security** | Minimal | CSP, XSS prevention, CSRF, auth patterns, OWASP coverage |
| **Performance** | Not considered | Core Web Vitals, caching strategies, N+1 prevention, indexing |
| **Type safety** | `any` creep | Strict TypeScript, branded types, zod validation, no `any` |
| **Testing** | Rarely included | Test pyramid, MSW, RTL, Playwright, AAA pattern |
| **Code quality** | Works but messy | Named conventions, SOLID, design patterns, anti-pattern awareness |
| **Completeness** | TODOs and stubs | Full implementations, no placeholders, production-ready |
| **Codex-native behavior** | Generic | Precision coding, code-first output, iteration patterns, function calling compatible |

---

## Project Structure

```
codex-skills/
├── README.md                  # This file
├── frontend-skills.md         # Frontend engineering prompt
└── backend-skills.md          # Backend engineering prompt
```

---

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/RHKfullstack/CODEX-SKILLS.git
cd CODEX-SKILLS
```

### Quick Start

1. Open the skill file you need:
   - `frontend-skills.md` — for frontend tasks
   - `backend-skills.md` — for backend tasks

2. Copy the entire contents.

3. Paste into ChatGPT, the OpenAI API system message, or a Custom GPT instructions field.

4. Start coding with a Principal-level engineer guiding the output.

### Stay Updated

```bash
git pull origin main
```

---

## Contributing

These prompts are living documents. If you find gaps, anti-patterns that should be added, or have suggestions for improvement:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Open a pull request with a clear description

Focus contributions on:
- Missing production concerns
- New framework versions and their best practices
- Anti-patterns that should be explicitly called out
- Better Codex/OpenAI-specific behavioral guidance

---

## Related Repositories

- [DEEPSEEK-SKILLS](https://github.com/RHKfullstack/DEEPSEEK-SKILLS) — The same prompts optimized for DeepSeek
- [CLAUDE-SKILLS](https://github.com/RHKfullstack/CLAUDE-SKILLS) — The same prompts optimized for Claude
- More AI platform-specific skills coming soon

---

## Roadmap

- [ ] `fullstack-skills.md` — Combined full-stack engineering prompt
- [ ] `devops-skills.md` — DevOps & infrastructure prompt
- [ ] `mobile-skills.md` — React Native / Flutter prompt
- [ ] `system-design-skills.md` — System design & architecture prompt
- [ ] `security-skills.md` — Dedicated application security prompt
- [ ] `code-review-skills.md` — Code review & PR review prompt

---

## License

MIT — Use, modify, and distribute freely. Attribution appreciated but not required.

---

<p align="center">
  <b>Built with ❤️ for engineers who want Codex/GPT to produce real production code.</b>
</p>