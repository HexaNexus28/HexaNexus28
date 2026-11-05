<p align="center">
  <a href="https://yawo-portfolio.vercel.app"><img src="assets/banner.svg" width="100%" alt="Yawo ZOGLO, software and AI developer, architect of the invisible"></a>
</p>

<p align="center">
  <a href="https://yawo-portfolio.vercel.app">Portfolio</a> ·
  <a href="https://www.linkedin.com/in/yawozoglo">LinkedIn</a> ·
  <a href="README.md">Version française</a>
</p>

<p align="center"><img src="assets/facts.svg" width="100%" alt="4 modules on a shared core, 4 open source projects, 8 routed AI providers, RLS multi-tenant isolation"></p>

Software and AI engineering apprentice at [ESIEA](https://www.esiea.fr), based in Paris.
**I build platforms, not pages**: a shared core (one database, one account, one error log), apps that plug into it,
and the infrastructure that keeps them running in production.
My line: *less but better*, and *if it's complicated, it's badly designed*.

<p align="center"><img src="assets/stack.svg" width="100%" alt="Stack: C#, .NET 9, ASP.NET Core, PHP, Laravel, Node.js, React 19, TypeScript, Vite, Tailwind, Electron, PostgreSQL, pgvector, Supabase, SQL Server, MariaDB, Ollama, Docker, Ansible, VPS, Vercel, CI/CD, Playwright"></p>

## The ShiftStar ecosystem

ShiftStar (challenges, votes and rankings for restaurants, in production since February 2026) is not a standalone
app: it is a core and modules that plug into it. SkillScan is one, others serve administration. They share one
database isolated per site (RLS), whose chosen access principle is to read under RLS and write through RPCs, and every
module's errors flow into a console. All of it runs on a
VPS managed with Ansible. The code is private, so here is the architecture.

<p align="center"><img src="assets/ecosystem.svg" width="100%" alt="Diagram: ShiftStar, SkillScan and internal modules around a shared core (Postgres, RLS, SSO, log); a console receives the errors; ORION has its own database; everything on a VPS"></p>

## Delivered products

Live products built for their owners. The code is theirs, so they are described here without being exposed.

<table>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/edusocialnews.jpg" width="56" height="56" alt="EduSocialNews logo"></td>
    <td><b><a href="https://edusocialnews.com">EduSocialNews</a></b><br>French-language education platform: articles, books, podcasts and quizzes. Moved in June 2026 from its former host to a Docker VPS.<br><sub>Laravel 9 · PHP 8.2 · MariaDB · Docker · Ansible</sub></td>
  </tr>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/la-magnificience.png" width="56" height="56" alt="La Magnificience logo"></td>
    <td><b>La Magnificience</b><br>SaaS of quizzes aligned with the official curriculum (APC) for Togolese middle schools: math formulas, geometry figures, and student progress that follows them across phones, including offline. In pilot.<br><sub>React 19 · Supabase · KaTeX · multi-tenant</sub></td>
  </tr>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/profilux.svg" width="56" height="56" alt="Profilux logo"></td>
    <td><b><a href="https://profilux.vercel.app">Profilux</a></b><br>One profile entered once, two outputs: a PDF resume that ATS systems actually read (selectable text, controlled reading order even in two columns, ATS score out of 100) and a public, indexed web portfolio in 6 themes.<br><sub>Next.js 15 · Supabase · react-pdf</sub></td>
  </tr>
</table>

## Open source

<table>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/rondo.svg" width="56" height="56" alt="Rondo logo"></td>
    <td><b><a href="https://github.com/HexaNexus28/Rondo">Rondo</a></b><br>YouTube music player in a borderless window or a 340 × 84 px mini card, always on top while you work. Ctrl+V adds a whole playlist; no account, nothing is collected.<br><sub>Electron · React 19 · Vite</sub></td>
  </tr>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/orion.svg" width="56" height="56" alt="ORION logo"></td>
    <td><b><a href="https://github.com/HexaNexus28/Orion">ORION</a></b><br>Personal AI assistant: 24 tools including Windows desktop actions, confirmation before any destructive action, long-term memory, and a decider that chooses to emit, defer or drop each notification.<br><sub>.NET 9 · React 19 · Three.js · pgvector</sub></td>
  </tr>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/pulsewatch.svg" width="56" height="56" alt="PulseWatch logo"></td>
    <td><b><a href="https://github.com/HexaNexus28/pulse-watch">PulseWatch</a></b><br>Tech watch: your RSS feeds, trends computed per category (TF-IDF) and a digest where an AI agent checks every claim against its sources before publishing.<br><sub>ASP.NET Core · React 19 · Google ADK</sub></td>
  </tr>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/nexus-switch.svg" width="56" height="56" alt="Nexus Switch logo"></td>
    <td><b><a href="https://github.com/HexaNexus28/nexus-switch">Nexus Switch</a></b><br>Launches Claude Code on 8 AI providers, free tiers first: models sorted cheapest-first, real cost shown before launch, keys protected by the OS.<br><sub>TypeScript · Ink · npm</sub></td>
  </tr>
</table>

## Hobbies

<p align="center"><a href="https://hexanexus28.github.io/Cosmos/kepler/"><img src="assets/kepler.png" width="760" alt="Kepler Planetarium: the real page, Solar System view. Halley's comet sweeps equal areas in equal times."></a></p>

**Kepler Planetarium**: planets of the Solar System up to the galaxy's central black hole, computed live from JPL data. [Open the simulation](https://hexanexus28.github.io/Cosmos/kepler/) The [Cosmos research notebook](https://github.com/HexaNexus28/Cosmos) extends the approach to the scale of the universe.

## Contact

[Portfolio](https://yawo-portfolio.vercel.app) · [LinkedIn](https://www.linkedin.com/in/yawozoglo)
