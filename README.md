# RealEstateWebsite

[![CI](https://img.shields.io/badge/CI-GitHub%20Actions-blue?logo=github)](https://github.com/<Zer0-Bug>/RealEstateWebsite/actions)
[![CodeQL](https://img.shields.io/badge/Code%20Scanning-CodeQL-orange)](https://github.com/<Zer0-Bug>/RealEstateWebsite/security/code-scanning)
[![Dependabot Status](https://img.shields.io/badge/Dependency%20Updates-Dependabot-green)](https://github.com/<Zer0-Bug>/RealEstateWebsite/pulse)
[![License: MIT](https://img.shields.io/badge/License-MIT-lightgrey.svg)](LICENSE)

A professional, production-oriented ASP.NET MVC real estate listing and management application. The project demonstrates a classical MVC architecture using ASP.NET MVC 5, Entity Framework 6, and SQL Server.

---

## Table of Contents

- [Overview](#overview)
- [Architecture & Tech Stack](#architecture--tech-stack)
- [Quick start](#quick-start)
- [Development workflow](#development-workflow)
- [CI / Security](#ci--security)
- [Contributing](#contributing)
- [License](#license)

## Overview

RealEstateWebsite is an ASP.NET MVC application that provides features for listing, searching, filtering and administering real estate listings. The project is built with a focus on clarity, extensibility, and compatibility with common Windows/.NET development tooling.

## Architecture & Tech Stack

- Framework: **ASP.NET MVC 5** (Target: **.NET Framework 4.7.2**)
- ORM: **Entity Framework 6.x** (code-first + initializers)
- Authentication: **ASP.NET Identity 2.x**
- Frontend: **Bootstrap 3/4** (CSS), **jQuery** (client behavior)
- Database: **Microsoft SQL Server** (backup available at `SQL Database/EmlakSite.bak`)
- Dev tooling: Visual Studio / GitHub (Actions, Dependabot, CodeQL)

Project structure highlights:

- `ASP.NET Project/RealEstateWebsite/` — main MVC application and solution (`.sln` / `.csproj`)
- `SQL Database/` — sample backup and database notes
- `Report/` — reporting utilities
- Static assets in `Content/` and `Scripts/`

## Quick start

Prerequisites:

- Windows 10 or 11
- Visual Studio 2019 (16.11+) or Visual Studio 2022 (recommended)
- .NET Framework 4.7.2 Developer Pack
- SQL Server 2017+ (or LocalDB)
- Git 2.30+

Clone and run locally:

1. Clone the repository:

   git clone https://github.com/<Zer0-Bug>/RealEstateWebsite.git

2. Open `ASP.NET Project/RealEstateWebsite.sln` in Visual Studio.
3. Restore NuGet packages (Visual Studio will prompt or run `nuget restore`).
4. Restore the DB backup `SQL Database/EmlakSite.bak` to a local SQL instance, or configure your own DB and update the connection string in `Web.config` (`<connectionStrings>`).
5. If you prefer to seed data with the project's initializers, ensure the connection string points to an empty DB and the initializer will run on first request.
6. Start debugging (IIS Express) from Visual Studio.

Tips:

- To run a build locally without Visual Studio: use MSBuild with the solution file.
- Keep secrets (connection strings, API keys) out of the repo; use environment variables or GitHub Secrets for Actions.

## Development workflow

- Branch strategy: `main` (protected), feature branches `feature/<short-desc>`, bugfix branches `fix/<issue-number>`.
- Pull requests: include a description, testing steps, and a short changelog.
- Use GitHub issues and projects to track work and priorities.

## CI / Security

This repository is designed to integrate with these GitHub features:

- GitHub Actions: run build + unit tests + static analysis on push/PR
- Dependabot: automated dependency updates
- CodeQL: code scanning for security vulnerabilities
- Security Policy & Issue Templates: for responsible disclosure

Suggested minimal workflow: `.github/workflows/ci.yml` with steps:
- restore packages
- build solution
- run tests (if added)
- run CodeQL analysis

## Contributing

Contributions are welcome. Suggested process:

1. Open an issue describing the change/bug.
2. Fork the repo and create a branch.
3. Run tests and linters locally.
4. Submit a pull request with a clear description and link to the issue.

Consider adding or using repository templates: ISSUE_TEMPLATE, PULL_REQUEST_TEMPLATE, CODE_OF_CONDUCT, and SECURITY.md.

## License

This project is released under the **MIT License** — see the `LICENSE` file for details.

---

> NOTE: This project is a demo/sample implementation intended for learning and evaluation. Do not use the demo data or bundled images in production without replacing them with appropriate assets and sanitized test data.
