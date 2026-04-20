---
title: Vercel Security Breach — What Happened and What You Should Do
date: 2026-04-20
categories: [Tech + AI]
tags: [vercel, security, data-breach, supply-chain, oauth, hacking, nextjs, developers]
image:
  path: /assets/images/vercel-breach.png
  alt: Vercel Security Breach April 2026
---

Cloud hosting giant Vercel confirmed this weekend that hackers breached its internal systems and accessed customer data — through a compromised third-party AI tool. Here's everything you need to know and the steps you should take right now.

## What Happened

### The Attack
- A Vercel employee installed **Context AI's Office Suite** app and connected it to their corporate Google Workspace account via OAuth
- A Context AI employee had been infected with **Lumma infostealer malware** in February 2026 (traced back to downloading Roblox "auto-farm" scripts)
- That infection exposed Context AI's credentials, including their Google OAuth tokens
- Hackers used the OAuth connection to **take over the Vercel employee's Google Workspace account**
- From there, they pivoted into Vercel's internal environments and accessed **unencrypted environment variables**

### What Was Stolen
- Customer API keys and environment variables (non-sensitive ones)
- Internal deployment credentials
- **580 Vercel employee records** — names, email addresses, account status, and activity timestamps
- Possibly source code and database data (claimed by the threat actor, unverified)

### Who's Selling the Data
A threat actor claiming to be **ShinyHunters** posted on BreachForums advertising the stolen data for **$2 million**, including API keys, source code, and access to internal deployments. The actual ShinyHunters group has denied involvement.

---

## What Is NOT Affected

| | |
|---|---|
| Next.js | ✅ Not affected |
| Turbopack | ✅ Not affected |
| Sensitive environment variables | ✅ Encrypted at rest, no evidence of access |
| On-chain crypto protocols (e.g. Orca) | ✅ Not affected |

---

## Timeline

| | |
|---|---|
| February 2026 | Context AI employee infected with Lumma infostealer |
| March 2026 | Context AI identifies and blocks unauthorized access to its AWS environment |
| April 17–19, 2026 | Hackers pivot into Vercel's internal systems via OAuth |
| April 19, 2026 | Vercel publicly discloses the breach |
| April 20, 2026 | Hudson Rock links breach to the February infostealer infection |

---

## Instructions for Vercel Users

### 1. Rotate your credentials
Immediately rotate all API keys, tokens, and secrets stored as environment variables in your Vercel projects — treat every non-sensitive variable as potentially compromised.

### 2. Audit your access logs
Review your Vercel project logs and Google Workspace audit logs for the window of **April 17–19, 2026** for any suspicious access or changes.

### 3. Check your Google Workspace for the malicious OAuth app
Go to **Google Admin Console → Security → API Controls → Manage Third-Party App Access** and search for this OAuth Client ID:
```
110671459871-30f1spbu0hptbs60cb4vsmv79i7bbvqj.apps.googleusercontent.com
```
If it appears, revoke access immediately.

### 4. Mark sensitive variables as "Sensitive"
In your Vercel dashboard, go to your project's Environment Variables settings and enable the **Sensitive** flag on any variable containing secrets. Sensitive variables are encrypted at rest and cannot be read back.

### 5. Audit third-party OAuth apps
Review every third-party tool connected to your Google Workspace or Vercel account. Remove any app you don't recognise or no longer use.

### 6. Inventory your CI/CD integrations
Check every tool with access to your CI/CD pipeline — npm tokens, GitHub tokens, deployment keys — and rotate anything that could have been exposed.

---

## Tips

- **Don't assume "non-sensitive" means safe** — API keys for databases, analytics tools, and services stored as plain environment variables are exactly what was exposed here.
- This is a classic **supply chain attack** — the hackers didn't break into Vercel directly; they went through a smaller third-party vendor first.
- Vercel has rolled out an improved **environment variables dashboard** — use it to get a clear overview of what's stored and what needs to be secured.
- If you're a **Web3 or crypto project** hosted on Vercel, be especially vigilant — wallet interfaces and RPC credentials stored as env vars could be high-value targets.
- For extra protection, consider using a **secrets manager** (e.g. AWS Secrets Manager, HashiCorp Vault) instead of storing sensitive credentials directly as environment variables.

---

## Incident Summary

| | |
|---|---|
| Disclosed | April 19, 2026 |
| Attack vector | OAuth supply chain via Context AI |
| Root cause | Lumma infostealer on a Context AI employee's machine |
| Data exposed | Employee records, API keys, env variables |
| Asking price on dark web | $2 million |
| Customers affected | "Hundreds of users across many organisations" (Vercel) |
| Next.js / Turbopack affected | No |
