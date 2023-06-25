FROM python:bookworm

WORKDIR /app

EXPOSE 5050

COPY Pipfile ./

RUN pip install pipenv
RUN pipenv lock
RUN pipenv install --system --deploy

COPY . ./

CMD [ "python", "main.py" ]