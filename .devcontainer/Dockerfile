FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:14
   
# configure npm and install global modules
RUN npm config set @sap:registry https://npm.sap.com \
    && npm i -g @ui5/cli \
    && npm i -g yo \
    && npm i -g generator-easy-ui5

# install Chrome for testing
RUN sudo apt-get update \
    && sudo apt-get install libxss1 libappindicator1 libindicator7 -y \
    && wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb \
    && sudo apt install ./google-chrome*.deb -y  	