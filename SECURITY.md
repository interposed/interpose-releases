# Security policy

## Supported versions

We support the most recent release. Older releases may still work but won't receive security fixes — upgrade when convenient.

| Version | Supported |
|---|---|
| latest released `v0.x.y` | ✅ |
| anything earlier | ❌ — please upgrade |

## Reporting a vulnerability

**Please do not open a public GitHub issue** for security vulnerabilities. Use one of these private channels instead:

- **Email:** `contact@stateful.art` with subject prefix `[interpose-security]`
- **GitHub Private Vulnerability Reporting:** click "Report a vulnerability" on this repo (`interposed/interpose-releases` → Security tab → Advisories → New draft). GitHub keeps the report private between you and the maintainer.

Include in your report:
- A description of the issue.
- The affected version (`interpose --version`).
- Steps to reproduce, ideally minimal.
- Your assessment of impact (RCE? privilege escalation? info leak? denial of service?).
- Whether you've discussed this with anyone else / disclosed publicly anywhere.

Acknowledgement target: **48 hours**. We'll confirm receipt, give a preliminary severity assessment, and outline next steps.

Fix target: depends on severity. Critical and exploitable issues get a release within **7 days** of acknowledgement; medium-severity within **30 days**; low-severity bundled into the next regular release.

## What we consider in-scope

- The interpose daemon binary itself (broker, enforcer, audit log, AAuth Person Server).
- The install script (`install.sh`) — supply-chain integrity of the install path is in scope.
- The bundled trust-list profiles — if a profile inadvertently trusts a binary that shouldn't be trusted in a typical agent context, that's in scope.
- Documentation that could lead a user to a less-secure configuration if followed literally.

## What's out of scope

- **Kernel bugs we can't fix** (e.g., LSM-BPF program detach via `CAP_BPF` — this is a documented limitation, see G8 in the architecture security notes; honest fix requires TPM-attested boot).
- **Userspace bypasses we acknowledge** — interpose's threat model is documented; vulnerabilities in scenarios the threat model explicitly excludes (e.g., root-already-compromised, malicious physical access, modified userspace that strips the agent's exec) are out of scope.
- **Theoretical issues without exploitation paths.** "An attacker who could do X could then do Y" requires X to be plausible.
- **Vulnerabilities in dependencies** that are already publicly known and tracked upstream — please file with the dependency author. We'll bump versions when fixes are available.

## Coordinated disclosure

We follow a standard coordinated-disclosure model:

1. You report privately.
2. We acknowledge within 48 hours and assess severity.
3. We work on a fix; you optionally participate in review.
4. We coordinate a public disclosure date — typically when the fix releases, with up to 90 days' grace for severe issues to allow patching across the user base.
5. We credit you in the release notes (unless you prefer anonymity — just say so).

If we don't respond within 7 days to your initial report, escalation is reasonable. Either reach out via the alternative channel above, or, if you've exhausted private channels and we're still silent past 30 days, public disclosure is your call.

## Hall of fame

This section will list reporters who have helped us improve interpose's security. (No one yet — be the first.)
