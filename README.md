# Lumina Home: example app for Percy QA triage

A small static storefront. It's the **app under test** for [`percy/example-percy-sdet-suite`](https://github.com/percy/example-percy-sdet-suite), a separate QA regression suite that snapshots it nightly with Percy.

It's there to try the **Percy Visual Testing Agent's QA workflow**: an SDET triages last night's regression run from their IDE. The agent explains each diff using the PRs merged into *this* repo since the last approved run.

You don't work in this repo directly. The suite's bootstrap forks it into your account and merges a couple of example PRs into your fork, so the nightly run has something to explain. See the suite repo's `BOOTSTRAP.md`.

```bash
npm install
npm run serve   # http://localhost:5500
```

The tag `baseline` marks the pristine state; the suite's `reset` script returns your fork's `main` to it.
