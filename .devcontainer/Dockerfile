# Java version: 17
ARG VARIANT=17
FROM mcr.microsoft.com/vscode/devcontainers/java:${VARIANT}

# Install Maven
ENV SDKMAN_DIR="/usr/local/sdkman"
ENV PATH=${SDKMAN_DIR}/bin:${SDKMAN_DIR}/candidates/maven/current/bin:${PATH}
COPY library-scripts/maven-debian.sh /tmp/library-scripts/
RUN apt-get update && bash /tmp/library-scripts/maven-debian.sh "latest" "${SDKMAN_DIR}"
