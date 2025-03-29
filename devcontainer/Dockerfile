FROM mcr.microsoft.com/devcontainers/ruby:3

# Install Jekyll
RUN gem install bundler jekyll

# Install additional dependencies
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    build-essential \
    git \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

# Set the default shell to bash
ENV SHELL /bin/bash