FROM eclipse-temurin:17-jdk

# Install Maven
RUN apt-get update && \
    apt-get install -y maven git curl unzip nano && \
    rm -rf /var/lib/apt/lists/*

# Create working directory
WORKDIR /app

# Default command (VS Code overrides this)
CMD ["bash"]
