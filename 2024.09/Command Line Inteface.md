# Digna Command Line Interface (CLI)

**Release 2024.09**

**2024-08-24**

---

## Table of Contents

- [Introduction](#introduction)
- [Purpose of the Command Line Interface (CLI)](#purpose-of-the-command-line-interface-cli)
- [Installation Instruction for Windows](#installation-instruction-for-windows)
- [CLI Basics](#cli-basics)
- [Using `help` Option](#using-help-option)
- [Using `check-repo-connection` Command](#using-check-repo-connection-command)
- [Using `version` Command](#using-version-command)
- [Using Logging Options](#using-logging-options)
- [User Management](#user-management)
  - [Using `add-user` Command](#using-add-user-command)
  - [Using `delete-user` Command](#using-delete-user-command)
  - [Using `modify-user` Command](#using-modify-user-command)
  - [Using `modify-user-pwd` Command](#using-modify-user-pwd-command)
  - [Using `list-users` Command](#using-list-users-command)
- [Repository Management](#repository-management)
  - [Using `upgrade-repo` Command](#using-upgrade-repo-command)
  - [Using `encrypt` Command](#using-encrypt-command)
  - [Using `generate-key` Command](#using-generate-key-command)
- [Data Management](#data-management)
  - [Using `clean-up` Command](#using-clean-up-command)
  - [Using `inspect` Command](#using-inspect-command)
  - [Using `tls-status` Command](#using-tls-status-command)
  - [Using `list-projects` Command](#using-list-projects-command)
  - [Using `list-ds` Command](#using-list-ds-command)

---

## Introduction

---

## Purpose of the Command Line Interface (CLI)

The DIGNA Command Line Interface (CLI) is a powerful tool designed to streamline interactions with the DIGNA platform. It provides a text-based interface that allows users to perform a wide range of tasks efficiently, without the need for a graphical user interface.

### Key Features:

- **Efficiency and Flexibility:** The CLI enables quick execution of commands, improving productivity.
- **Automation:** Supports scripting to automate repetitive tasks.
- **Remote Access:** Manage DIGNA resources from anywhere.
- **Consistency and Reliability:** Ensures reliable operations with documented, version-controlled commands.
- **Scalability:** Handles large-scale operations for enterprise tasks.
- **Learning and Mastery:** Provides deeper understanding of DIGNA's functionality.
- **Integration with Other Tools:** Seamlessly integrates with automation tools like Control-M, UC4, AutomateNOW!

---

## Installation Instruction for Windows

1. **Extracting the Digna CLI:**
   - Obtain the `.zip` file containing the Digna CLI.
   - Unzip the file to your desired directory.

2. **Deploying the `dignacli` Folder:**
   - Copy the `dignacli` folder to your preferred installation location (e.g., `C:\Program Files\digna`).

3. **Configuring `config.toml`:**
   - Check for `config.toml` inside `dignacli`.
   - Rename `config_template.toml` to `config.toml` if needed and configure it using the provided documentation.

---

## CLI Basics

---

## Using `help` Option

The `--help` option provides information about available commands and their usage. There are two main ways to use this option:

1. **Displaying General Help:**
   ```bash
   dignacli --help

2.  **Getting Help for Specific Commands:**  
  For detailed information about a specific command, append `--help` to that command. For example, to obtain help with the `add-user` command, run:

