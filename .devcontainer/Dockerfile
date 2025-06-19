FROM eclipse-temurin:17-jdk

# Install Maven
RUN apt-get update && \
    apt-get install -y maven git curl unzip nano && \
    rm -rf /var/lib/apt/lists/*

# Create working directory
WORKDIR /app

# Generate SSH key (without passphrase) for the container user
RUN ssh-keygen -t rsa -b 4096 -f /root/.ssh/id_rsa -N "" -q
RUN eval "$(ssh-agent -s)" && \
    ssh-add /root/.ssh/id_rsa

# Default command (VS Code overrides this)
CMD ["bash"]
