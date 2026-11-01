# AFP website

Source for [agentfiles.org](https://agentfiles.org), the website of the Agent Files Protocol (AFP).

The site is one static page, `index.html` (Tailwind from its CDN, no build step, no analytics): the problem, the idea, the operations and error codes, backends, AMP integration, security, and an install quickstart. Next to it are `404.html`, `robots.txt`, `sitemap.xml`, `site.webmanifest`, `llms.txt`, `humans.txt` and `.well-known/security.txt`.

## Deployment

GitHub Pages serves the `main` branch from the repository root (Settings > Pages: deploy from a branch, `main`, `/`), the same setup as agentids.org. `CNAME` holds the custom domain, `agentfiles.org` (DNS at Cloudflare). `.nojekyll` turns off Jekyll, which would otherwise drop `.well-known/`. Every push to `main` redeploys the site.

## Editing

Edit the files directly and open a pull request. To preview, serve the folder locally, for example `python3 -m http.server`, and open http://localhost:8000.

The page describes the protocol; it must match the specification and the reference scripts. When the spec changes, update `index.html` and `llms.txt` together, and bump `<lastmod>` in `sitemap.xml`.

## Specification

The protocol specification and the reference client (`afp-*.sh`, `install.sh`, the Claude Code skill) live at [agentmessaging/agent-files](https://github.com/agentmessaging/agent-files) (v0.1 draft).

## Related

- [AMP](https://agentmessaging.org): Agent Messaging Protocol
- [AAP](https://agentactions.org): Agent Actions Protocol
- [AID](https://agentids.org): Agent Identity Protocol
- [AI Maestro](https://ai-maestro.23blocks.com): first provider

## License

MIT.
