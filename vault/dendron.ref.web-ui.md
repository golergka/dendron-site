---
id: 25287595-96bb-410b-ab46-eb9a26b0e259
title: Web UI
desc: ''
updated: 1625167081470
created: 1621552722494
---

## Summary
- status: [[Experimental 🧪|dendron.ref.status#experimental-🧪]]

The Dendron Web UI refers to Dendron's native UI components build using the latest web technologies (instead of VSCode components).
This lets us create dynamic interfaces with dynamic dropdowns, drag and drop and custom made components. 

## Quickstart

To get started, set [[enableWebUI|dendron.topic.config.dendron#enablewebui]] to true and then reload your workspace to enable.

## Components

### TreeView

This is an implementation of the [[Dendron Tree View|dendron.topic.workbench#dendron-tree-view]] using the Dendron Web UI. 

### Calendar View

The Dendron Calendar View lets you view your daily journal in calendar form.

<!-- TODO: picture -->
The Dendron Calendar View has the following capabilities:

- Clicking on a given day date will open the corresponding daily journal note
- Clicking on a given day without a daily journal note will create one
- Days without daily journal note are grayed out and days that contain an entry are displayed in white.
- Shows indicators in the form of dots (max 5) to reflect the word count of that entry. Each dot repesents 250 words.
- Switching between month/year view
- In a multi-vault workspace it shows the daily journal from the vault associated with the active note

- NOTE: the calendar view will only work if you have default `journal` settings in your `dendron.yml`
    ```yml
    journal:
        dailyDomain: daily
        name: journal
        dateFormat: y.MM.dd
        addBehavior: childOfDomain
    ```

#### Configuration

##### journal.firstDayOfWeek
- default: 0

Set start of week (eg. `0` for sunday, `1` for monday, `2` for tuesday, etc.)  for the [[Dendron Calendar View|dendron.topic.workbench#calendar-view]]

### Preview
- [[Experimental 🧪|dendron.ref.status#experimental-🧪]]

The Dendron Preview gives you a rich HTML preview for your notes. Currently it is missing the following features compared to the current [[preview|dendron.topic.preview]]:
- mermaid diagrams
- scroll sync

If you discover any issues that are not listed above, please submit a bug repo [here](https://github.com/dendronhq/dendron/issues/new?assignees=&labels=&template=bug_report.md&title=) so we can add it to our roadmap!
#### Methods

##### Show Preview V2
Brings up the native Dendron Preview

## Theming

Dendron Web UI supports a dark and light theme and will switch according to your current IDE theme. If you switched themes, you'll need to run `Reload Window` for Dendron to update its theme
