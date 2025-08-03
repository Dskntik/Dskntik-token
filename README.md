TON FunC Codespace Setup
This repository is a GitHub Codespace-ready setup for working with TON blockchain smart contracts in FunC and Fift.
What's included

Ubuntu 22.04 container
func and fift compilers
toncli tool
Sample contract: contracts/hello.fc

Getting Started

Open this repository in Codespaces:
Click the Code button on GitHub and select Open with Codespaces.
Create a new Codespace or use an existing one.


Wait for the container to build and initialize.
Use the terminal to run toncli commands or work with FunC/Fift files in the contracts directory.

Troubleshooting

If the Codespace fails to start, check the .devcontainer/devcontainer.json and Dockerfile for errors.
Ensure all dependencies (toncli, func, fift) are installed by running toncli --version in the terminal.
If you encounter issues, rebuild the container via the Codespaces menu (gear icon > Rebuild Container).
