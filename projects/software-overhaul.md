---
title: Software Overhaul | Projects
layout: page
---

# Software Overhaul
AWDE uses a bunch of different tools and software and we're wanting to move toward a more systematic
and self-owned environment.

**STATUS: Inactive**

## Specific Goals

  + Documentation
    + Single schelling document overview of all currently used group tools, sites, and platforms
    + Style guides and best practices document
  + Hosting (should all be self-hosted (local or cloud), dockerized, built from source, and
    automatically backed up)
    + [Media wiki](https://www.mediawiki.org/wiki/MediaWiki)
    + [Gitea](https://gitea.io/en-us/)
    + [Matrix Synapse](https://matrix.org/docs/projects/server/synapse)
  + Bots
    + Calendar Bot
      + Can connect to the Discord, Matrix, or an arbitrary web endpoint
      + Can use multiple calendars
      + Features
        + Reminders (with customizable specific times and output locations)
        + Summaries (weekly, monthly, etc)
        + Changed/Moved/Deleted notifications
        + Event creation (and 'find a time' wizard)
    + Activity Wizard
      + Guided creation process for a new event, project, or group
      + Authorized users can activate/deactivate activities, unauthorized can create in deactivated
        state
    + Democracy Bot
      + Can run votes with a variety of methods (plurality, approval, ranked pref, quadratic)
      + Can optionally automatically trigger scripts based on vote result (including sending actions
        to the calendar bot or activity wizard)