FROM python:3

WORKDIR /usr/src/app
COPY app.py ./

RUN pip install --no-cache-dir flask uwsgi

# CMD ["python", "app.py"]
CMD ["uwsgi", "--socket", "my-app.sock", "--http", "0.0.0.0:8000", "--wsgi-file", "app.py", "--callable", "app"]