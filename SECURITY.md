# Security policy

## Reporting a vulnerability

Please do **not** open a public issue for a security problem.

Use GitHub's private reporting instead — **Security → Report a vulnerability**
on the affected repository — or email **kulshreshtha.surya@engineer.com** with
`SECURITY` in the subject.

Please include the repository and commit, what an attacker could do, and the
smallest reproduction you have. A proof of concept is welcome but not required.

I aim to acknowledge within **72 hours** and to agree a disclosure timeline with
you before anything is published. These are personal projects, not a funded
product, so please read that as a good-faith commitment rather than an SLA.

## Scope

These repositories are learning and portfolio projects. They are not hardened
for production and should not be deployed as-is. That said, the following are
genuinely in scope and I want to hear about them:

- **ForkablePlaywrightSelfHealer** executes generated test code and talks to a
  local model. Anything that escapes the offline network guard, or turns a
  natural-language spec into unintended code execution, is a real finding.
- Any workflow that could leak `GITHUB_TOKEN`, a secret, or an artifact
  containing credentials.
- Any dependency or GitHub Action pinned in a way that permits substitution.
- Credentials or tokens committed to history.

## Out of scope

- Test credentials for public practice sites, which those sites publish
  themselves.
- Missing hardening on code explicitly documented as a learning example.
- Automated scanner output with no demonstrated impact.
