# Contributing to 0G Proxy

Thanks for your interest in contributing! Here's how to get started.

## Development Setup

```bash
git clone https://github.com/claraverse-space/0G-Compute-Adapter.git
cd og-proxy
npm install
cp .env.example .env
# Edit .env with your 0G private key
node server.js
```

## Project Structure

This is intentionally a **single-file server** (`server.js`). This is a design choice, not a limitation — it keeps the project minimal, easy to understand, and simple to deploy. Please don't split it into modules unless there's a compelling reason discussed in an issue first.

## Making Changes

1. Fork the repo and create a branch from `main`
2. Make your changes in `server.js` or `public/index.html`
3. Test your changes locally with a real 0G wallet
4. Submit a pull request

## Code Style

- ES modules (`import`/`export`)
- No TypeScript (keeping it simple)
- Use the existing comment banner style for sections (`// -- Section Name --`)
- No unnecessary dependencies — the entire proxy runs on 3 packages

## What We're Looking For

- New tool call format parsers (the models keep inventing new ones)
- Better prompt engineering for tool calling reliability
- Support for new 0G models as they come online
- Dashboard UI improvements
- Documentation and examples

## Reporting Issues

- Use GitHub Issues
- Include the request that caused the error
- Include relevant log entries (from `/api/logs` or the JSONL files)
- Never include your private key or API keys in issues

## Security

See [SECURITY.md](SECURITY.md) for reporting vulnerabilities.
