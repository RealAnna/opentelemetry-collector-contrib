FROM mcr.microsoft.com/mssql/server:2025-latest@sha256:245f6b1c8903edae52cb20fa31419cefcde1a49938bb8c3447099011fc871ca3

ENV ACCEPT_EULA=Y
ENV SA_PASSWORD=YourStrong!Passw0rd

# Set the working directory
WORKDIR /usr/src/app

# Copy the scripts and set the executable permissions before copying them into the image
COPY entrypoint.sh configure-db.sh init.sql ./

ENTRYPOINT ["/bin/bash", "/usr/src/app/entrypoint.sh"]