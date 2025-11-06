# Use a specific Python version that has better wheel support
FROM mcr.microsoft.com/devcontainers/python:3.11-bullseye

# Install build dependencies needed for PyArrow (just in case)
RUN apt-get update && apt-get install -y \
    cmake \
    build-essential \
    libssl-dev \
    libffi-dev \
    libbz2-dev \
    liblzma-dev \
    && rm -rf /var/lib/apt/lists/*

# Set the working directory in the container
WORKDIR /workspace

# Copy the requirements.txt file to the container
COPY requirements.txt .

# Install the dependencies from requirements.txt
RUN pip install --no-cache-dir -r requirements.txt
