---
title: Software Overhaul | Projects
layout: page
---

# Software Overhaul
AWDE uses a bunch of different tools and software and we're wanting to move toward a more systematic
and self-owned environment.

**STATUS: Active; Thursdays AST plus one weekend from 2021-02-18 to 2021-05-13 for 11 meetings in
total**

## Goals

### Initial Goals

  + Documentation
    + Single schelling document overview of all currently used group tools, sites, and platforms
    + Style guides and best practices document
  + Hosting (should all be self-hosted (local or cloud), dockerized, built from source, and
    automatically backed up)
    + [Media wiki](https://www.mediawiki.org/wiki/MediaWiki)
    + [Gitea](https://gitea.io/en-us/)
    + [Matrix Synapse](https://matrix.org/docs/projects/server/synapse)
  + Bots
    + Bot Framework
      + Can handle core IO logic (read/respond to comments)
      + Standardized debugging for convenience
      + Custom "Bot Interfaces" to work with Discord, Matrix, et al
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

### Future Goals

  + Hosting
    + [Discourse](https://www.discourse.org/) (tentative)
    + [Next Cloud](https://nextcloud.com/) (tentative; explore other filesharing options first)
  + Bots
    + Media Bot
      + Embeding unfriendly sites (tiktok...)
  + Tools
    + Sysadmin dashboard
  + Explore
    + Matrix peer-to-peer?

## Multi-Stage Project
This project is going to operate in a few stages to cover the amount of work that needs to be done.

### Stage 1

  1. Hosting (AWS)
    1. Script
      + Setting up
      + Updating
      + Shutting down
      + Renewing certs
      + Checking health
      + Backing up
  2. Documentation
    + Software stack
    + How-to/FAQ for common procedures
  3. Bot Framework + Simple Test Bot
    + Core library with idiomatic addressing (so specific servers can be referenced by name without
      caring about what protocol they use)
    + Wrap up common IO into protocol (sending and receiving messages, etc)
    + Templated project setup (possibly use [cookiecutter](https://github.com/cookiecutter/cookiecutter))

Script-as-we-go; document-as-we-go

#### Meeting 1 (2021-02-18 AST)
Host Media Wiki and Gitea

#### Meeting 2
Fully script Media and Gitea

#### Meeting 3
Hosting Synapse

#### Meeting 4
Fully script Synapse and create 'general' scripts

#### Meeting 5 + Homework
Write all documentation (homework, lots of this can be done over the week)

#### Meeting 6; Hackathon Lite (2021-03-27 and 2021-03-28)
Try to build the framework and test bot semi-blind; aggressively record gripes

Downtime between 6 and 7

#### Meeting 7 (2021-04-15 AST)
Architecture Planning for Bot Framework

#### Meeting 8 + Homework
Write core library

#### Meeting 9 + Homework
Write IO protocol

#### Meeting 10 + Homework
Project template

#### Meeting 11 (2021-05-13 AST)
Wrap-up/Catch-up

### Stage 2
  
  1. Calendar Bot

### Stage 3

  1. Activity Wizard
  2. Democracy Bot
