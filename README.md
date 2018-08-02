# After-installing-ubuntu
if have an intel chip and your screen freezes do the following

1) ```sudo nano /etc/default/grub```
Then find a line with ```GRUB_CMDLINE_LINUX_DEFAULT="quiet splash" ```

and replace it with ```GRUB_CMDLINE_LINUX_DEFAULT="quiet splash intel_idle.max_cstate=1"```

CTRL + X and save it before exiting the file


# Installing NVM (Node version manager)
The reason for using nvm instead of other install types is mainly in how easy it is to have multiple versions of Node.js (if needed) without too much of extra complexity. Sometimes applications might require a certain version of Node.js to work, so having the flexibility of using specific versions can save a lot of time from you.

1) Open new Terminal window.
2) Run nvm installer

     ...with either curl or wget.
         ```curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash```
        OR ``` wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash```

3) List what versions of Node are currently installed (probably none).
    ```nvm ls```
4) Install latest Node.js LTS release (recommended for production usage).
     ```nvm install v8.11.3``` or any other required version, just change the version
  
5) Set a default Node version for nvm (enabling you to actually use it in a new Terminal session windows).
   ```nvm alias default v8.11.3 (when you work with production quality projects)```
   
   If require help, run ```nvm help``` or if require any other version just install them accordingly to ```help``` guide

