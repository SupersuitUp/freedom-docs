---
name: upgrade-freedom-framework
description: Locate and fetch the current Freedom upgrade ledger. The full ledger is served to Freedom clients from the client repo; this public file carries the version list so that every installed workspace can tell whether it is behind without needing credentials.
---

# Freedom Upgrade Ledger — version index

**Latest version: v3.0.0**

This file is public on purpose, and it is deliberately thin.

Every installed Freedom workspace polls this URL **unauthenticated** at session start to decide
whether to tell its owner they are behind. That check has to keep working for someone whose
access has lapsed, or whose install is years old — those are precisely the people who most need
to be told a newer version exists. So the version list lives here, in the open, forever.

The upgrade INSTRUCTIONS are not here. They are served to Freedom clients, who have read access to
the client repo because that access is how Freedom is installed in the first place.

## Getting the full ledger

```bash
gh api repos/SupersuitUp/freedom/contents/UPGRADE-LEDGER.md \
  -H "Accept: application/vnd.github.raw"
```

If that returns 404, the GitHub account you are authenticated as is not a Freedom client. That is
the wall, and it is the only one — nothing here is obfuscated, and the skills themselves are
plain markdown on your own disk once installed.

Not a client yet: https://github.com/SupersuitUp/freedom

## Versions

Newest last. An upgrade applies every entry between the installed version and the latest, in
order.
### → v2.0.0 (Freedom, formerly PAOS)
### → v2.0.1 (the migration command was wrong)
### → v2.1.0 (message-contact can address a group)
### → v2.2.0 (message-contact is now send-message)
### → v2.3.0 (nothing outside the workspace knew who CiCi was)
### → v2.4.0 (activate is the front door: state aware, replaces, and hands off to onboard)
### → v2.5.0 (a stale config filename was silently discarding whole path maps)
### → v3.0.0 (the agent is Freedom, and its soul is stated)
