FROM python:3.12-slim

# This is based on https://github.com/trr266/otree3_docker/blob/master/Dockerfile

ENV APP_DIR /app

RUN apt-get update && \
    apt-get install -y git && \
    python3 -m venv .venv && \
    source .venv/bin/activate && \
    pip install --upgrade pip && \
    pip install otree

COPY src .

CMD ["otree", "prodserver", "src", "8000"]
