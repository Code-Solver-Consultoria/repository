FROM debian:trixie

RUN apt update && \
	apt install -y maven ant sudo git git-flow openjdk-25-jdk zsh zsh-theme-powerlevel9k

RUN useradd -c 'VSCode Desenv User' -m -p vscode -s /bin/zsh vscode

ARG USERNAME=vscode
RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME
	
# Set `DEVCONTAINER` environment variable to help with orientation
ENV DEVCONTAINER=true
ENV ZSH_THEME="powerlevel9k/powerlevel9k"
