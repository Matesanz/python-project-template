# VSCode Base Image
FROM mcr.microsoft.com/vscode/devcontainers/python:0-${PYTHON_VERSION}

# Install Poetry
RUN pip install "poetry==1.1.14"

# Install python dependencies using poetry
COPY pyproject.toml /
RUN cd / && poetry config virtualenvs.create false \
    && poetry install --no-interaction --no-ansi
