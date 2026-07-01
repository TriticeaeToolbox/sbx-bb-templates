FROM docker.io/docker/sandbox-templates:claude-code-docker

USER root

RUN apt-get update && apt-get install -y python3-openpyxl python3-pandas

USER agent

RUN claude plugin marketplace add TriticeaeToolbox/t3-marketplace && \
    claude plugin install generate-breedbase-templates@t3-marketplace