FROM python:3.9-slim

# Install required packages
RUN apt-get update && \
    apt-get install -y ffmpeg && \
    pip install --no-cache-dir yt-dlp

# Create working directory
WORKDIR /downloads

# Create a non-root user
RUN useradd -m -u 1000 dluser && \
    chown -R dluser:dluser /downloads

USER dluser

# Set the entrypoint to yt-dlp
ENTRYPOINT ["yt-dlp"]