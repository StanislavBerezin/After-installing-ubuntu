# After-installing-ubuntu


# Installing NVM (Node version manager)
The reason for using nvm instead of other install types is mainly in how easy it is to have multiple versions of Node.js (if needed) without too much of extra complexity. Sometimes applications might require a certain version of Node.js to work, so having the flexibility of using specific versions can save a lot of time from you.

Open new Terminal window.
Run nvm installer
...with either curl or wget.
        curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
        wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
  The script clones the nvm repository to ~/.nvm and adds the source line to your profile (~/.bash_profile, ~/.zshrc, ~/.profile, or ~/.bashrc). (You might want/need to add the source loading line by yourself, if the automated install tool does not add it for you.)
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
If everything went well, you should now be able to reload the shell by running
source ~/.bashrc
(Another option is to open a new Terminal window/tab.)
Verify installation
To verify that nvm has been installed, do: command -v nvm
List what versions of Node are currently installed (probably none).
nvm ls
Install latest Node.js LTS release (recommended for production usage).
nvm install v8.11.3
Install Current Node.js release with latest features (for testing the future features of Node).
nvm install v10.7.0
Set a default Node version for nvm (enabling you to actually use it in a new Terminal session windows).
nvm alias default v8.11.3 (when you work with production quality projects)
nvm alias default v10.7.0 (ONLY if you want to test the latest features of Node.js. Please note that some packages are broken with the latest Node v10.)
