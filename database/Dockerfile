# Use the official Ubuntu image as the base image
FROM ubuntu:latest

# Install necessary packages to set up Cosmos DB emulator
RUN apt-get update \
    && apt-get install -y \
        apt-transport-https \
        curl \
    && curl https://packages.microsoft.com/keys/microsoft.asc | apt-key add - \
    && curl https://packages.microsoft.com/config/ubuntu/20.04/prod.list > /etc/apt/sources.list.d/microsoft-prod.list \
    && apt-get update \
    && apt-get install -y \
        azure-cosmos-emulator \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Expose the port used by the Cosmos DB emulator
EXPOSE 8081

# Command to start the Cosmos DB emulator when the container starts
CMD ["cosmosdb-emulator"]
