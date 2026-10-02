# ShellGrid, a lightweight terminal organizer for Windows

A simple way to run and organize multiple terminals in one window, and to send AI
agents to work in them while you watch.

## Demo

https://github.com/user-attachments/assets/b57023ed-e110-4d9d-b832-ee14dc11dc40


## Why it exists

Working with multiple terminals on Windows can get messy. You open a few shells, move them around, change folders, and try to keep everything organized across your screen.

There are terminal managers that solve this, but many of them come with a lot of features and overhead. ShellGrid keeps things simple. It gives you one window for your terminals and lets you arrange everything yourself.

## What it does

- **Start Claude or Codex automatically.** Open a new terminal with Claude or Codex already running.
- **Move and resize terminals.** Drag panes around, split them, and arrange them however you want.
- **Choose the working directory.** Pick the folder before launching a terminal, so it opens exactly where you need it.
- **Use layout presets.** Create 2x2, 3x3, or 4x4 terminal layouts with one click.
- **Float a workspace.** Drag a tab out of the tab bar to pop it into its own window, and dock it back when you're done.

## New in 2.0: let your agent run the agents

Ask Claude (or Codex) to split a job across several agents, for example *"Using ShellGrid, open 5 agents and give each one a different test file to fix"*, and ShellGrid opens a grid of real terminals, one agent per pane, each with its own task. Your agent waits for them to finish and reads their results. You watch it all happen on screen.

- **One click to connect.** ShellGrid registers itself with Claude Code or Codex for you. Then start a new session.
- **A little progress buddy.** The sidebar shows how the agents are doing (*working, 3 of 5 done*), and each pane gets a badge: working, done, or needs you.
- **You stay in charge.** If an agent needs an answer, ShellGrid tells you and takes you to it. Folder-trust prompts ("Do you trust this folder?") can only be answered by you.

## Built with Rust

ShellGrid is built with Tauri 2, using Rust for the backend and WebView2 for the interface. There is no Electron and no bundled browser.

The terminals are real Windows shells running through ConPTY via Rust (`portable-pty`). Each terminal runs independently, so if one process gets busy or stuck, the others keep running normally.

The whole app is a single ~5 MB program that starts quickly and uses little memory. It is also its own connection to Claude and Codex, so there is nothing else to install.

## Download

Get **ShellGrid_2.0.0_x64-setup.exe** from the [Releases](../../releases) page and run it. It installs just for your user, with no admin rights needed.

Requires Windows with WebView2 (built into Windows 11). To use the agent features, have Claude Code or Codex installed and signed in.

ShellGrid isn't code-signed yet, so Windows SmartScreen may show "unknown publisher" the first time. Click *More info → Run anyway*.

**Heads-up on permissions:** agents that ShellGrid starts for your Claude session run with Claude's permission prompts skipped, so they can run commands and edit files in their folder without asking. Point them at projects you're comfortable with that for.

ShellGrid is free to use. It is not open source.
