FROM  ghcr.io/ffxivita/docker-dalamud:latest

# Optout of telemtry.
ENV DOTNET_CLI_TELEMETRY_OPTOUT=1
ENV DOTNET_SKIP_FIRST_TIME_EXPERIENCE=1

# Create a non-root dev user.
RUN adduser --disabled-password --gecos "" dev

# Install required dependencies.
RUN apk add --update openssh

# Download the repository into /workspaces (overwrote if using a compliant tool).
WORKDIR /workspaces 
RUN git clone https://github.com/DarkArtek/XIVITASanctuary.git