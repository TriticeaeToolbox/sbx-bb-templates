FROM docker.io/docker/sandbox-templates:claude-code-docker

USER agent

RUN pip install xlrd openpyxl pandas -q --break-system-packages

RUN claude plugin marketplace add TriticeaeToolbox/t3-marketplace && \
    claude plugin install generate-breedbase-templates@t3-marketplace
