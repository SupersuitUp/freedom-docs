---
name: upgrade-freedom-framework
description: Locate and fetch the current Freedom upgrade ledger. The full ledger is served to Freedom clients from the client repo; this public file carries the version list so that every installed workspace can tell whether it is behind without needing credentials.
---

# Freedom Upgrade Ledger — version index

**Latest version: v4.56.0**

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
### → v4.15.0 (the work log reads git, because skill invocations were never the work)
### → v4.16.0 (your evening work stops disappearing, and a release updates the machine that cut it)
### → v4.17.0 (one definition of "today", and it is your computer's)
### → v4.18.0 (the signals collector, computed here and inspectable before anything is sent)
### → v4.19.0 (signals are sent, and whoami stops promising a secrecy the product never offered)
### → v4.20.0 (a project can be a practice, and can live in another repo)
### → v4.21.0 (an inspo board you own: one file per item, no server, no key)
### → v4.21.1 (an item saved late at night is dated today, not tomorrow)
### → v4.21.2 (a saved page keeps its description and image)
### → v4.22.0 (what's next, answered from the project files and with its reasons)
### → v4.23.0 (one image skill, two providers, a recipe on every render)
### → v4.23.1 (the image craft ships with the image skill)
### → v4.23.2 (the chunk model is gone from the prose too)
### → v4.24.0 (send-message attaches images, and proves they arrived)
### → v4.24.1 (the attachment path imports what it uses)
### → v4.24.2 (attachments send with the screen locked)
### → v4.25.0 (attachments to groups)
### → v4.26.0 (groups are records in the PRM)
### → v4.26.1 (the do-not-contact check reads the whole frontmatter)
### → v4.27.0 (the time of day is read, never inferred)
### → v4.27.1 (the login code reaches you during the wait, not after it)
### → v4.27.2 (your commits carry your name, and `report-upstream` is now `suggest-an-improvement`)
### → v4.28.0 (connect every Google account you have, in one flow, and never be told about the wrong one)
### → v4.28.1 (`connect-google --status` actually reports status)
### → v4.29.0 (give the agent a logged-in browser without closing your tabs)
### → v4.30.0 (the doctor notices you cannot open your own recordings)
### → v4.31.0 (saving now notices what was MISSING, not only what was wrong)
### → v4.31.1 (update-freedom stops telling you there is no file layer when there is)
### → v4.32.0 (an update stops pulling the floor out from under the session, and a lapsed capture gets noticed)
### → v4.33.0 (start-here is now initialize-session, and one skill writes project state)
### → v4.34.0 (Freedom refuses to run until the machine is activated and linked, and every skill is now a draft)
### → v4.34.1 (activate stops breaking the shell profile it was repairing)
### → v4.35.0 (the installer stops before the agent exists, and the installers ship on release)
### → v4.35.1 (the first line of a session greets the person, not the fetch)
### → v4.36.0 (the version is derived, not remembered)
### → v4.37.0 (the release calls update-freedom instead of reimplementing it)
### → v4.38.0 (the opener stops claiming your work is unsaved)
### → v4.39.0 (the profile opens on this week, and you can press it)
### → v4.40.0 (the wiki reference is behind your Freedom account, and your links open it)
### → v4.40.1 (the checkup counted your artifacts as zero if you filed them in folders)
### → v4.40.2 (the checkup told you to install something without saying where from)
### → v4.41.0 (your projects can live under more than one root)
### → v4.41.1 (the iMessage check graded the window you opened, not your Mac)
### → v4.42.0 (the moment worth saving is the moment it gets lost)
### → v4.43.0 (you can message a group without naming it first)
### → v4.44.0 (bring a friend into their own learning wiki)
### → v4.45.0 (a door into the detoiling loop, and a version check that stops lying)
### → v4.45.1 (a contributor could not see the gate their PR would fail)
### → v4.45.2 (open the PR, do not offer to open it)
### → v4.46.0 (your projects can now trigger your own steps)
### → v4.47.0 (a call two people recorded is still one meeting)
### → v4.48.0 (the editor, and the refusal that makes it safe)
### → v4.49.0 (two silent failures an operator found in the first hour)
### → v4.50.0 (the launcher change that can actually reach you, and two projects to start from)
### → v4.51.0 (three reports that had been waiting on a decision, all built)
### → v4.52.0 (reopening the editor picks your conversation back up, and Google Docs works on default settings)
### → v4.53.0 (you can upgrade the editor from inside the editor)
### → v4.54.0 (one terminal on open, always a fresh session)
### → v4.55.0 (the installer looks at your screen instead of taking its own word for it)
### → v4.56.0 (a skill you write is global, or it is not a skill)
