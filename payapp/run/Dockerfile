FROM erlang:latest

# Install the released application
COPY artifacts/mgsv /mgsv

# Install less
RUN apt-get update && \
    apt-get install -y less

# Expose relevant ports
EXPOSE 8080
EXPOSE 8443
CMD ["/mgsv/bin/mgsv", "foreground"]