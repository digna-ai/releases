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

To get started, follow the steps outlined below to extract the necessary files, deploy the 
dignacli folder, and configure your connection to the Digna repository. Ensure you have 
your repository credentials and any required configuration details ready before you begin.

1. **Extracting the Digna CLI:**
   - Obtain the `.zip` file containing the Digna CLI.
   - Unzip the file to your desired directory.

2. **Deploying the `dignacli` Folder:**
   - Copy the `dignacli` folder to your preferred installation location (e.g., `C:\Program Files\digna`).

3. **Configuring `config.toml`:**
   - Check for `config.toml` inside `dignacli`.
   - Rename `config_template.toml` to `config.toml` if needed and configure it using the provided documentation.

Your Digna CLI setup should now be complete. For advanced configuration and usage, refer 
to the full documentation or contact support at support@digna.ai


---

## CLI Basics

---

## Using `help` Option

The `--help` option provides information about available commands and their usage. There are two main ways to use this option:

1. **Displaying General Help:**
   
    Use –help immediate after the keyword dignacl  
   ```bash
   dignacli --help

3.  **Getting Help for Specific Commands:**  
  
    For detailed information about a specific command, append `--help` to that command.
    For example, to obtain help with the `add-user` command, run:
     ```bash
     dignacli add-user --help
     ```

     **Output**:
      
     **Command Description:** Offers a detailed description of what the command does.  
     **Syntax:** Shows the exact syntax, including required and optional arguments.  
     **Options:** Lists any options specific to the command, along with their explanations.  
     **Examples:** Provides examples of how to execute the command effectively.

  
## Using `check-repo-connection` Command

The check-repo-connection command is a utility within the DIGNA CLI tool designed to test the connectivity and access to a specified DIGNA repository. This command ensures that the CLI can interact with the repository.
      
**Command Usage:**
```bash
dignacli check-repo-connection
```

Upon successful execution, the command outputs a confirmation of the connection, along with details about the repository: Repository version, Host, Database and Schema.  
  
If the repository connection is not successful, check the config.toml file for correct configuration settings.

## Using ‘version’ command

To check the installed version of dignacli, use the --version option.  
  
**Command Usage:**
```bash
dignacli --version
```
  
**Example Output**
```bash
dignacli version 2024.09
```

## Using logging options
  
By default, the console output of the Digna commands is designed to be minimalistic. Most commands offer the possibility of providing additional information, using the following options:  
  
-- verbose (-v)
-- debug (-d)
-- logfile (lf)
  
“verbose” and “debug” are defining the level of detail, whereas the “logfile” switch allows redirecting the output to be streamed to a file rather than the console window.

  
  
