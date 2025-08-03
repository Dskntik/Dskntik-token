TON FunC Codespace Setup
This repository is a GitHub Codespace-ready setup for working with TON blockchain smart contracts in FunC and Fift.
What's included

Ubuntu 22.04 container
func and fift compilers (from TON CLI tools)
Sample contract: contracts/hello.fc

Getting Started

Open this repository in Codespaces:
Click the Code button on GitHub and select Open with Codespaces.
Create a new Codespace or use an existing one.


Wait for the container to build and initialize (this may take a few minutes due to TON compilation).
Verify func and fift are installed by running:func -V
fift -V

Expected output:func version: 0.4.0 (or newer)
fift version: 0.4.0 (or newer)


Use the terminal to run func or fift commands, or work with FunC/Fift files in the contracts directory.

Example Commands

Compile a FunC contract:func -o output.fif -SPA contracts/hello.fc


Run a Fift script:fift -s output.fif



Troubleshooting

If the Codespace fails to start, check the .devcontainer/devcontainer.json and Dockerfile for errors.
If func or fift commands are not found, rebuild the container:
Go to the Codespaces menu (gear icon) and select Rebuild Container.


If compilation fails, ensure all dependencies are installed. Check the build logs in the Codespaces creation output.
If issues persist, contact the repository maintainer or open an issue on GitHub.
