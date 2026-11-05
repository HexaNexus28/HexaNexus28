<p align="center">
  <a href="https://yawo-portfolio.vercel.app">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
      <source media="(prefers-color-scheme: light)" srcset="assets/banner-light.svg">
      <img src="assets/banner-dark.svg" width="100%" alt="Yawo Zoglo, développeur logiciel et IA : plateformes multi-tenant, agents IA, infrastructure">
    </picture>
  </a>
</p>

<p align="center">
  <a href="https://yawo-portfolio.vercel.app">Portfolio</a> ·
  <a href="https://www.linkedin.com/in/yawozoglo">LinkedIn</a> ·
  <a href="README.en.md">English version</a>
</p>

Étudiant-apprenti développeur logiciel et IA à l'[ESIEA](https://www.esiea.fr).
**Je construis des plateformes, pas des pages** : un noyau partagé (une base, un compte, un journal d'erreurs), des
applications qui s'y branchent, et l'infrastructure qui les fait tenir en production.
Ma ligne : *moins mais mieux*, et *si c'est compliqué, c'est mal conçu*.

<p align="center"><img src="assets/stack.svg" width="100%" alt="Stack : C#, .NET 9, ASP.NET Core, PHP, Laravel, Node.js, React 19, TypeScript, Vite, Tailwind, Electron, PostgreSQL, pgvector, Supabase, SQL Server, MariaDB, Ollama, Docker, Ansible, VPS, Vercel, CI/CD, Playwright"></p>

## L'écosystème ShiftStar

ShiftStar (challenges, votes et classements pour la restauration, en production depuis février 2026) est la brique centrale d'une
plateforme : SkillScan évalue les compétences avec le même compte, une console suit les sites et les erreurs, un site vitrine et
sa documentation sont publics. Le principe qui tient l'ensemble : **un tenant est un site**. Une organisation regroupe des sites
et ne les franchit que par un chemin explicite, jamais en assouplissant la règle d'isolation. L'isolation est portée par la base
(RLS et trigger d'écriture), et un script de conformité exécutable vérifie ce modèle avant et après chaque mise en production.
Les frontends sont sur Vercel, les données sur un VPS auto-hébergé (Supabase, depuis octobre 2026) géré par Ansible. Le code est
privé : voici l'architecture.

<p align="center"><img src="assets/ecosystem.svg" width="100%" alt="Architecture : les frontends sur Vercel (ShiftStar, SkillScan, console, site vitrine) parlent à une couche de données auto-hébergée sur un VPS (Postgres avec RLS, authentification unique, temps réel, fonctions) ; à droite, la frontière de données : chaque site est un tenant, une organisation les regroupe et les franchit par un chemin explicite"></p>

## Produits livrés

Des produits en ligne pour des commanditaires. Leur code leur appartient, je les décris sans l'exposer.

<table>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/edusocialnews.jpg" width="56" height="56" alt="Logo EduSocialNews"></td>
    <td><b><a href="https://edusocialnews.com">EduSocialNews</a></b><br>Plateforme éducative francophone : articles, livres, podcasts et quiz. Migrée en juin 2026 de son ancien hébergeur vers un VPS Docker.<br><sub>Laravel 9 · PHP 8.2 · MariaDB · Docker · Ansible</sub></td>
  </tr>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/la-magnificience.png" width="56" height="56" alt="Logo La Magnificience"></td>
    <td><b>La Magnificience</b><br>SaaS de quiz alignés sur le programme officiel (APC) des collèges togolais : formules mathématiques, figures géométriques et progression de l'élève qui le suit d'un téléphone à l'autre, y compris hors ligne. En pilote.<br><sub>React 19 · Supabase · KaTeX · multi-tenant</sub></td>
  </tr>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/profilux.svg" width="56" height="56" alt="Logo Profilux"></td>
    <td><b><a href="https://profilux.vercel.app">Profilux</a></b><br>Un profil saisi une fois, deux sorties : un CV en PDF que les ATS lisent vraiment (texte sélectionnable, ordre de lecture contrôlé même en deux colonnes, score ATS sur 100) et un portfolio web public indexé, en 6 thèmes.<br><sub>Next.js 15 · Supabase · react-pdf</sub></td>
  </tr>
</table>

## Open source

<table>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/rondo.svg" width="56" height="56" alt="Logo Rondo"></td>
    <td><b><a href="https://github.com/HexaNexus28/Rondo">Rondo</a></b><br>Lecteur de musique YouTube en fenêtre sans bordure ou en mini-carte de 340 × 84 px, au premier plan pendant que vous travaillez. Ctrl+V ajoute une playlist entière ; sans compte, rien n'est collecté.<br><sub>Electron · React 19 · Vite</sub></td>
  </tr>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/orion.svg" width="56" height="56" alt="Logo ORION"></td>
    <td><b><a href="https://github.com/HexaNexus28/Orion">ORION</a></b><br>Assistant IA personnel : 24 outils dont les actions du poste Windows, confirmation avant toute action destructive, mémoire à long terme, et un décideur qui choisit d'émettre, de différer ou d'écarter chaque notification.<br><sub>.NET 9 · React 19 · Three.js · pgvector</sub></td>
  </tr>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/pulsewatch.svg" width="56" height="56" alt="Logo PulseWatch"></td>
    <td><b><a href="https://github.com/HexaNexus28/pulse-watch">PulseWatch</a></b><br>Veille technologique : vos flux RSS, des tendances calculées par catégorie (TF-IDF) et un digest où un agent IA vérifie chaque affirmation contre ses sources avant publication.<br><sub>ASP.NET Core · React 19 · Google ADK</sub></td>
  </tr>
  <tr>
    <td width="76" valign="top"><img src="assets/logos/nexus-switch.svg" width="56" height="56" alt="Logo Nexus Switch"></td>
    <td><b><a href="https://github.com/HexaNexus28/nexus-switch">Nexus Switch</a></b><br>Lance Claude Code sur 8 fournisseurs d'IA, gratuits d'abord : modèles triés du moins cher au plus cher, coût réel affiché avant le lancement, clés protégées par le système.<br><sub>TypeScript · Ink · npm</sub></td>
  </tr>
</table>

## Hobbies

<p align="center"><a href="https://hexanexus28.github.io/Cosmos/kepler/"><img src="assets/kepler.png" width="760" alt="Planétaire Kepler : la page réelle, vue Système solaire. La comète de Halley balaie des aires égales en des temps égaux."></a></p>

**Planétaire Kepler** : les planètes du Système solaire jusqu'au trou noir central de la galaxie, calculées en direct à partir des données du JPL. [Ouvrir la simulation](https://hexanexus28.github.io/Cosmos/kepler/) Le [carnet de recherche Cosmos](https://github.com/HexaNexus28/Cosmos) prolonge la démarche à l'échelle de l'univers.

## Contact

[Portfolio](https://yawo-portfolio.vercel.app) · [LinkedIn](https://www.linkedin.com/in/yawozoglo)
