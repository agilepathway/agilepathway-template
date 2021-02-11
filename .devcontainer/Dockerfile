FROM mcr.microsoft.com/vscode/devcontainers/universal:linux

COPY scripts/* /tmp/scripts/

USER root

RUN HADOLINT_VERSION=$(go run /tmp/scripts/hello.go) \
    && /tmp/scripts/install-hadolint.sh "$HADOLINT_VERSION" \
    # && /tmp/scripts/install-gauge.sh \
    && rm -rf /tmp/scripts

USER codespace
