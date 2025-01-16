# Devbox Setup Guide

This README file provides instructions for setting up Devbox on your system. Devbox is a powerful tool that helps manage development environments, making it easier to work on projects with specific dependencies and configurations.

## Prerequisites

Before you begin, ensure that you have the following:

- A Debian-based Linux distribution (e.g., Ubuntu).
- Sufficient permissions to install packages and run scripts.

## Installation Steps

Follow these steps to install Devbox and configure your environment:

### Step 1: Update Package Lists

Open your terminal and run the following command to update your package lists. This ensures that you have the latest information about available packages:

```bash
sudo apt update
```

### Step 2: Install Required Packages

Next, install the necessary packages for running Devbox. This includes `curl`, `nano`, and `xz-utils`. Run the following command:

```bash
sudo apt install curl nano xz-utils
```

- **curl:** A command-line tool for transferring data with URLs.
- **nano:** A simple text editor for editing configuration files.
- **xz-utils:** A set of tools for handling `.xz` compressed files, required by Devbox.

### Step 3: Install Devbox

Now, you can install Devbox using the following command:

```bash
curl -fsSL https://get.jetify.com/devbox | bash
```

This command downloads and executes the installation script for Devbox. Follow any prompts that may appear during the installation process.

### Step 4: Configure Devbox

After installation, you need to create or edit a configuration file named `devbox.json`. This file defines the packages and settings for your development environment.

To create or edit this file, use the following command:

```bash
nano devbox.json
```

You can add your desired packages and configurations in this JSON file. Here’s an example of what your `devbox.json` might look like:

```json
{
    "packages": [
        "python@12",
        "node@20",
        "git",
        "fzf"
    ],
    "init_hooks": [
        "echo 'Welcome to your Devbox environment!'"
    ]
}
```

### Step 5: Start Your Devbox Shell

Once you have configured your `devbox.json`, you can start a new Devbox shell by running:

```bash
devbox shell
```

This command will initialize your development environment based on the configurations specified in `devbox.json`.

## Additional Information

For more details on how to use Devbox, including adding packages and managing environments, refer to the official [Devbox documentation](https://www.jetify.com/docs/devbox).

## Conclusion

You have successfully installed and configured Devbox on your system! You can now manage your development environments more efficiently. If you encounter any issues or have questions, feel free to reach out or consult the documentation. Happy coding!