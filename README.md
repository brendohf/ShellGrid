# ShellGrid, a lightweight terminal organizer for Windows

A simple way to run and organize multiple terminals in one window.

## Demo

<video src="https://github.com/brendohf/ShellGrid/releases/download/v1.0.0/demo.mp4" controls width="100%"></video>

[Watch the demo](https://github.com/brendohf/ShellGrid/releases/download/v1.0.0/demo.mp4)

## Why it exists

Working with multiple terminals on Windows can get messy. You open a few shells, move them around, change folders, and try to keep everything organized across your screen.

There are terminal managers that solve this, but many of them come with a lot of features and overhead. ShellGrid keeps things simple. It gives you one window for your terminals and lets you arrange everything yourself.

## What it does

- Start Claude or Codex automatically. Open a new terminal with Claude or Codex already running.
- Move and resize terminals. Drag panes around, split them, and arrange them however you want.
- Choose the working directory. Pick the folder before launching a terminal, so it opens exactly where you need it.
- Use layout presets. Quickly create 2x2, 3x3, or 4x4 terminal layouts with one click.

## Built with Rust

ShellGrid is built with Tauri 2, using Rust for the backend and WebView2 for the interface. There is no Electron and no bundled browser.

The terminals are real Windows shells running through ConPTY via Rust (`portable-pty`). Each terminal runs independently, so if one process gets busy or stuck, the others keep running normally.

The entire application is a single 4.6 MB executable. It starts quickly, uses little memory, and does not require an installer.

## Download

Get the latest ShellGrid.exe from the [Releases](../../releases) page. It is a single portable file, no installer.

Requires Windows with WebView2 (built into Windows 11).
