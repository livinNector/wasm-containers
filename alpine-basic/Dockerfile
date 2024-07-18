FROM alpine:latest

# Install essential packages
RUN apk update && apk add --no-cache \
    bash \
    build-base \
    openjdk11-jdk \
    python3 \
    python3-dev \
    py3-pip \
    wget \
    curl \
    iputils

# Create symbolic links for python and pip
RUN ln -sf python3 /usr/bin/python \
    && ln -sf pip3 /usr/bin/pip

# Verify installations
RUN bash --version && \
    gcc --version && \
    g++ --version && \
    javac -version && \
    python --version && \
    pip --version && \
    wget --version && \
    curl --version && \
    ping -V

# Set bash as the default shell
CMD ["bash"]
