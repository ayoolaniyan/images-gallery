FROM python:3.9-rc-slim

WORKDIR /app

EXPOSE 5050

COPY Pipfile Pipfile.lock ./

RUN pip install --upgrade pip
RUN pip --no-cache-dir install pipenv
RUN pipenv requirements --dev > requirements.txt
RUN pip install -r requirements.txt

COPY . ./

CMD [ "python", "main.py" ]