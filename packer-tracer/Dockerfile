# -----------------------------
# Base image
FROM ubuntu:22.04
ARG DEBIAN_FRONTEND=noninteractive

# -----------------------------
# Set working directory
WORKDIR /home/dev
ENV TZ=Europe/Rome
# -----------------------------
# Install essential packages
RUN apt update && apt install -y --no-install-recommends \
    sudo curl wget git zsh locales x11-apps \
    build-essential pkg-config libssl-dev software-properties-common \
    dialog xdg-utils gtk-update-icon-cache \
    libnss3 libxss1 libxslt1.1 libxcb-xinerama0-dev gnome \
    && locale-gen en_US.UTF-8 \
    && apt clean && rm -rf /var/lib/apt/lists/*

# -----------------------------
# Create user and group
RUN groupadd -f wireshark \
    && useradd -m -s /usr/bin/zsh dev \
    && echo "dev ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers \
    && usermod -aG wireshark dev \
    && chown -R dev:dev /home/dev

WORKDIR /home/dev

# -----------------------------
# Switch to dev user
USER dev

# -----------------------------
# Set aliases
RUN echo 'alias lg="eza --icons -l --git"' >> ~/.bashrc \
    && echo 'alias lt="eza --icons -l --tree --git"' >> ~/.bashrc

# -----------------------------
# Install Helix editor via PPA
USER root
RUN apt update && apt install -y software-properties-common \
    && add-apt-repository -y ppa:maveonair/helix-editor \
    && apt update \
    && apt install -y helix \
    && apt clean && rm -rf /var/lib/apt/lists/*

# -----------------------------
# Copy local .deb files
COPY Packet_Tracer822_amd64_signed.deb /tmp/
# -----------------------------
# Install Packet Tracer and HUB
RUN apt update #\
    && apt install -y /tmp/Packet_Tracer822_amd64_signed.deb

# -----------------------------
# Final working directory
WORKDIR /home/dev
