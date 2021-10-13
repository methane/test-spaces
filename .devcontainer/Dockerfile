FROM mcr.microsoft.com/vscode/devcontainers/universal:1-linux

COPY library-scripts/*.sh /tmp/library-scripts/
RUN bash /tmp/library-scripts/common-debian.sh \
    && bash /tmp/library-scripts/python-debian.sh

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends bash-completion \
        default-libmysqlclient-dev default-mysql-client default-mysql-server
