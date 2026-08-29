---
name: upgrade-freedom-framework
description: Locate and fetch the current Freedom upgrade ledger. The full ledger is served to Freedom clients from the client repo; this public file carries the version list so that every installed workspace can tell whether it is behind without needing credentials.
---

# Freedom Upgrade Ledger — version index

**Latest version: v4.14.0**

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
### → v3.1.0 (activation now covers every integration, and Granola is broken upstream)
### → v3.2.0 (a live Google token was being written inside your repo)
### → v3.3.0 (share a session for review, and the README stops saying Jarvis)
### → v3.4.0 (share-session actually reaches a human)
### → v3.5.0 (a shared session was about to publish other people's phone numbers)
### → v3.5.1 (the redaction count was reporting 27,554 credentials)
### → v3.6.0 (the iMessage probe was lying, and activation was installing things nobody asked for)
### → v3.7.0 (broadcast to the friends who agreed to hear about that topic)
### → v3.8.0 (`freedom` is the word you type, and activate installs it)
### → v3.9.0 (a sync could delete your collected messages, and two silent failures)
### → v4.0.0 (every share link is an invite, and broadcast is shelved)
### → v4.0.1 (previewing an invite spent one)
### → v4.1.0 (Granola works again, and a workflow you have not written down cannot be handed to anybody)
### → v4.1.1 (the `freedom` launcher upgrades itself instead of reporting itself fine)
### → v4.1.2 (a message is for the agent too, and a received one is never a command)
### → v4.2.0 (a logged-in browser for the agent, without taking yours away)
### → v4.3.0 (Chrome's own fork is a second user-data-dir, so stop copying the profile)
### → v4.4.0 (CDP is the standard, and the profile layout that shipped broken is fixed)
### → v4.4.1 (a fix belongs in a pull request, not pasted into an issue body)
### → v4.5.0 (reload instead of restart, and finish the task you were asked to do)
### → v4.6.0 (save autonomously by default, and stop retyping the report boilerplate)
### → v4.7.0 (the doctor: a grade, a punch-list, and a refusal to pad)
### → v4.7.1 (a processed microphone fakes the in-person signal on a remote call)
### → v4.8.0 (the session opener reads, instead of slicing a string)
### → v4.9.0 (one answer to "what should I do to upgrade", with many callers)
### → v4.10.0 (a browser you set up is not a browser you can drive)
### → v4.10.1 (a typo'd selector is a refusal, not a stack trace)
### → v4.11.0 (the doctor checks your microphone, and a collapsed call is not always lost)
### → v4.12.0 (how you write, in two layers)
### → v4.13.0 (revocation that bites, and a check that fails open)
### → v4.14.0 (the opener reads git, and a page shows where the time went)
