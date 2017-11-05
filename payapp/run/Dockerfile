FROM erlang:latest

# Install the released application
COPY artifacts/mgsv /mgsv

# Expose relevant ports
EXPOSE 8080
EXPOSE 8443
CMD ["/mgsv/bin/mgsv", "foreground"]