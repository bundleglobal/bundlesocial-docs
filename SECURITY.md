# Security Policy

## Supported Versions

bundle.social is a hosted service, so the API and dashboard always run the current
version - there are no older deployments to patch. For the client libraries we ship
fixes to the latest release of the current major line.

| Component                                    | Supported                                    |
| -------------------------------------------- | -------------------------------------------- |
| bundle.social API and dashboard (hosted)     | :white_check_mark: current deployment        |
| `bundlesocial` (Node SDK) 2.x                | :white_check_mark: latest release            |
| `bundlesocial-cli` 1.x, `bundlesocial-mcp` 1.x | :white_check_mark: latest release          |
| Client libraries, older majors               | :x:                                          |

Self-hosting is not supported, so pinning an old SDK version does not keep you on an
old API. If you are affected by a fix in a client library, upgrade to its latest release.

## Reporting a Vulnerability

Please report security issues privately - do not open a public GitHub issue, pull
request, or discussion.

Reach us through [bundle.social/contact](https://bundle.social/contact) with "security"
in the subject, and we will move the report to a private channel with the engineers who
own the affected area.

A useful report includes what you found, the affected endpoint, page, or package, the
steps to reproduce it, and what an attacker could do with it. Proof-of-concept code and
request/response captures help a lot. If you need to share something sensitive, say so
and we will arrange an encrypted channel rather than having you paste it into a form.

### What to expect

- **Acknowledgement** within 3 business days.
- **Initial assessment** - whether we can reproduce it and how we are rating it -
  within 7 business days.
- **Progress updates** at least every 7 days while the report is open.
- **If accepted**, we fix it and tell you when the fix is live. Timelines depend on
  severity: critical issues are handled immediately, lower-severity ones ship with
  regular releases. You will get credit in the [changelog](https://info.bundle.social/changelog)
  if you want it, and we are happy to stay anonymous if you prefer.
- **If declined**, you get an explanation of why - usually out of scope, working as
  intended, or already known and tracked.

### Scope

In scope: the bundle.social API, the dashboard, the hosted connect portal, the
official SDK/CLI/MCP packages, and this documentation site.

Out of scope: findings in the social platforms we integrate with (report those to
Meta, Google, TikTok, X, and so on through their own programs), denial-of-service and
volumetric testing, spam or social engineering against our staff or users, missing
hardening headers with no demonstrated impact, and automated scanner output without a
working proof of concept.

### Ground rules

When testing, please use your own organization and your own connected accounts. Do not
access, modify, or exfiltrate other customers' data or their social accounts, and do
not publish to accounts you do not own. Stop as soon as you have confirmed a
vulnerability, and give us a reasonable window to ship a fix before disclosing
publicly. Research that follows these rules is welcome, and we will not pursue action
over it.
