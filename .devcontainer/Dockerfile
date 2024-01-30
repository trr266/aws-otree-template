FROM python:3.12-slim

# This is based on https://github.com/trr266/otree3_docker/blob/master/Dockerfile

ENV APP_DIR /app

RUN pip install otree

CMD ["otree", "prodserver", "8000"]
