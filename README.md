# DataArcus for Power BI: releases

Release files for **DataArcus for Power BI**, a local MCP server that lets Claude plan, check and write Power BI
reports (PBIP) on your own computer, after you approve each plan. It writes Arabic reports right to left, one report
with an English/Arabic language button, and a Gulf calendar (weekends by country, Ramadan and Eid, Hijri months).

- **Source code:** https://github.com/Antnioo/DataArcus
- **About the beta and how to join:** https://dataarcus.com/power-bi-mcp/ (Arabic: https://dataarcus.com/ar/power-bi-mcp/)
- **What changed in each version:** the release notes, from [mcp/CHANGELOG.md](https://github.com/Antnioo/DataArcus/blob/main/mcp/CHANGELOG.md)

## Before you install: check the file

Each release lists the SHA-256 of its `.mcpb` file in its notes and in `SHA256SUMS`. Check yours matches before you
install it. On Windows:

```
certutil -hashfile "dataarcus-0.3.0.mcpb" SHA256
```

or in PowerShell: `Get-FileHash "dataarcus-0.3.0.mcpb"`. If the two values differ, don't install it.

## Install

You need Windows, Claude Desktop and Power BI Desktop 2.159.883.0 (October 2026) or later. With Claude Desktop
installed, double-click the `.mcpb` file and choose Install (if Windows asks which app opens it, choose Claude). Or, in
Claude Desktop: Settings > Extensions > Advanced settings > Install Extension..., then pick the file. The full steps,
including the working folder and how to update or remove it, are in
[mcp/README.md](https://github.com/Antnioo/DataArcus/blob/main/mcp/README.md).

## Privacy

DataArcus has no telemetry and makes no network connections of its own, and it writes nothing until you click
Approve in its approval window. What its tools return is read by Claude (so it goes to Anthropic under your Claude
account): your model's structure (table, column and measure names, types, formats), never the rows of your tables, plus
the short texts typed in a report (titles, text boxes). Details:
[mcp/PRIVACY.md](https://github.com/Antnioo/DataArcus/blob/main/mcp/PRIVACY.md). The download counts on this page are
GitHub's own.

## Licence

See [LICENSE](https://github.com/Antnioo/DataArcus/blob/main/LICENSE) in the source repository. Not open source: you
may use the reports, themes and scripts it generates for you for any purpose, including commercial work; the software
itself may not be copied, modified or redistributed without written permission.

Questions and feedback: through the beta page above.
