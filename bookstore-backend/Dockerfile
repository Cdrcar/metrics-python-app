FROM python:3.8-slim-buster

RUN pip3 install pipenv

ENV PROJECT_DIR /usr/src/flaskbookapi

WORKDIR ${PROJECT_DIR}

COPY Pipfile .
COPY api.py .
COPY LICENCE .
# COPY Pipfile.lock .  UPDATED Dockerfile so it does not include to Lock file
# COPY . .

RUN pipenv install --deploy --ignore-pipfile

EXPOSE 5000

CMD ["pipenv", "run", "python", "api.py"]