# Use the official Python base image
FROM python:3.10-slim

# Set a working directory
WORKDIR /app

# Copy application files to the container
COPY . /app

# Install system dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    libgl1-mesa-glx \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Install Python dependencies from requirements.txt
RUN pip install --no-cache-dir --upgrade pip && pip install --no-cache-dir -r requirements.txt

# Expose the port that Gradio uses
EXPOSE 7860

# Set the entry point to run your Python app
CMD ["python", "demo.py"]
