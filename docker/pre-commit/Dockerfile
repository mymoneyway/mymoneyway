FROM python:3.13.3-slim-bookworm

WORKDIR /mmw

# Install necessary system packages and tools
RUN apt-get update && \
    apt-get install --no-install-recommends -y \
        wget=1.21.3-1+deb12u1 \
        git=1:2.39.5-0+deb12u2 && \
    wget -qO go.tar.gz https://dl.google.com/go/go1.24.0.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go.tar.gz && \
    rm go.tar.gz && \
    wget -qO /bin/hadolint https://github.com/hadolint/hadolint/releases/download/v2.12.0/hadolint-Linux-x86_64 && \
    chmod +x /bin/hadolint && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set up Go path
ENV PATH="/usr/local/go/bin:${PATH}"

# Install Python dependencies and set up pre-commit
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt && \
    git init && \
    pre-commit install

CMD ["/bin/bash"]
