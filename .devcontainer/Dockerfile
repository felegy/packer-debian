# [Choice] Debian version (use bullseye on local arm64/Apple Silicon): bullseye, buster
ARG VARIANT=bullseye
FROM mcr.microsoft.com/vscode/devcontainers/base:${VARIANT}

# ** [Optional] Uncomment this section to install additional packages. **
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

USER vscode
RUN \
mkdir -p $HOME/.ssh && chmod 700 $HOME/.ssh; \
echo 'Host github.com \n\
  Hostname ssh.github.com \n\
  Port 443 \n\
  User git \n\
\n\
Host gist.github.com \n\
  Hostname ssh.github.com \n\
  Port 443 \n\
  User git \n\
'>  $HOME/.ssh/config
USER root

