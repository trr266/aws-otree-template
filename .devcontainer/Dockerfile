FROM python:3.12-slim

# This is based on https://github.com/trr266/otree3_docker/blob/master/Dockerfile

WORKDIR /app

COPY requirements.txt .

RUN apt-get update && \
    apt-get install -y git curl && \
    curl -LsSf https://astral.sh/uv/install.sh | sh && \
    source $HOME/.local/bin/env && \
    uv pip install -r requirements.txt --system

COPY src /app/

CMD ["otree", "prodserver", "8000"]
