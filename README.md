# Mergewell — Git Conflict Resolver

Welcome to the official support page for **Mergewell**, a lightweight tool that helps developers detect, inspect, and resolve Git merge conflicts quickly and safely.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [System Requirements](#system-requirements)
- [Getting Started](#getting-started)
- [Using Mergewell](#using-mergewell)
	- [Detecting Conflicts](#detecting-conflicts)
	- [Resolving Conflicts](#resolving-conflicts)
	- [Command Line Usage](#command-line-usage)
- [Troubleshooting](#troubleshooting)
- [Frequently Asked Questions (FAQ)](#frequently-asked-questions-faq)
- [Contact Support](#contact-support)
- [Privacy & Security](#privacy--security)
- [Version Information](#version-information)

---

## Overview

**Mergewell** is a cross-platform helper for resolving Git merge conflicts. It provides a clear overview of conflicted files, a simple side-by-side diff view, and easy actions to accept one side, keep both edits, or edit manually. Mergewell aims to reduce the time spent untangling merge problems and to make conflict resolution less error-prone.

---

## Features

- **Conflict Detection**: Scans the current Git repository for files with merge conflict markers.
- **Side-by-side Diff View**: Presents `HEAD` vs incoming changes with clear conflict regions.
- **Hunk Actions**: Accept current change, accept incoming change, accept both, or open the hunk in an editor.
- **Auto-Stage Resolved Files**: Optionally stage files after resolution to streamline commits.
- **Safe Preview**: Shows what the file will look like after applying a chosen resolution before making changes.
- **Lightweight & Local**: All operations happen locally; no files are uploaded to external services.

---

## System Requirements

- **macOS**: 11.0 (Big Sur) or later
- **Memory**: 512MB minimum (1GB recommended)

---

## Getting Started

1. **Download & Install**
	 - Visit the Releases page on the repository to download prebuilt binaries for your platform, or build from source.
2. **Open a Repository**
	 - Run Mergewell inside a Git working copy (or point it at a repo or file path).
3. **Start Resolving**
	 - Let Mergewell scan for conflicts and follow the UI/CLI prompts to resolve them.

---

## Using Mergewell

### Detecting Conflicts

- Run the scanner from the app or use the CLI command `mergewell scan` to list conflicted files.
- Mergewell detects standard Git conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`) and shows file context.

### Resolving Conflicts

- Open a conflicted file in Mergewell to see a side-by-side comparison of `HEAD` and the incoming change.
- For each conflict hunk you can:
	- **Accept Current**: Keep the `HEAD` version.
	- **Accept Incoming**: Keep the incoming change.
	- **Accept Both**: Concatenate both sides in a sensible order.
	- **Edit Manually**: Open the hunk in your default editor to craft a custom resolution.
- After resolving all hunks in a file, choose **Mark Resolved** (and optionally **Stage File**) to prepare it for commit.

---

## Troubleshooting

- **No conflicts found but Git reports one**:
	- Ensure you are running Mergewell in the repository root or pass the repository path.
	- Run `git status` to confirm conflict state.
edits.
- **Resolutions not applied**:
	- Make sure you clicked **Mark Resolved** to write changes.
	- Check file permissions and that is able to write the working tree.

---

## Frequently Asked Questions (FAQ)

Q: What file types does Mergewell work with?

A: Mergewell works with any text-based file where Git produces conflict markers (source code, config files, text). It is not intended for binary file content merging.

Q: Can Mergewell automatically commit resolutions?

A: Mergewell can not stage resolved files or auto-commit by default. This keeps require manual operations.


---

## Contact Support

If you need help or want to report a bug, please open an issue on the repository or contact the maintainer:

- **Repository**: https://github.com/idoo/Mergewell
- **Email**: ivan@0x.se

---

## Privacy & Security

Mergewell performs all operations locally on your machine and does not transmit repository contents externally. The tool may read files in your working tree and call Git as a subprocess.

---

## Version Information

- **Current Version**: 0.1.0
- **Release Date**: 2026-01-23

For release notes and updates, see the Releases page on the repository.

---

Thank you for using Mergewell. If you'd like, I can also add example CLI usage, a quickstart GIF, or a CONTRIBUTING section.