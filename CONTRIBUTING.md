# Contributing

These repositories exist to be forked. Contributions are welcome, and so is
taking the code and going your own way — that is what the name means.

## Before you open a pull request

Every repository here is a test-automation project, so the bar is a little
different from a typical codebase: **the tests are the product**. A change that
makes the suite pass without making it more truthful is a regression.

Three rules carry most of the weight:

1. **A test must fail when the thing it tests is broken.** Break the feature,
   watch it go red, then fix it back. A test that has never failed has never
   been verified.
2. **No hard waits.** `time.sleep()` and `waitForTimeout()` are timing bets that
   will lose on a slower runner. Use auto-waiting or an explicit expectation.
3. **No order dependency and no shared mutable data.** If your test only passes
   when run after another one, it is not a test, it is a step. Everything must
   survive `-n 4`.

## Getting set up

Each repository's README has a 60-second quickstart. If it does not work on a
fresh clone with no environment variables set, that is a bug worth reporting on
its own — a fork must go green on the first run.

## Commit messages

Say what was wrong and why it mattered, not just what changed. The diff already
shows what changed.

```
Bound the locator timeout when walking the candidate ladder

_try_candidate inherited the page's 5s default, so eight candidates for one
missing element cost 40s before healing even started. A candidate that is not
on the page is never *slowly* not on the page.
```

## Reporting a flaky test

Use the **Flaky test** issue template. It asks for the node ID and the observed
failure rate because those are the two things that make the report actionable.

A flaky test is worse than no test: it trains people to ignore red. The fix is
to quarantine it and find the cause — not to add a retry and move on.

## Security

Do not open a public issue for a security problem. See [SECURITY.md](SECURITY.md).

## Licence

Unless a repository says otherwise, contributions are accepted under that
repository's licence (MIT in every case). By opening a pull request you confirm
you have the right to contribute the code.
