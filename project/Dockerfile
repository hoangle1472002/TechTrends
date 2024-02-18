FROM python:3.8

WORKDIR /app

COPY ./project/techtrends .
RUN pip install --no-cache-dir -r /app/requirements.txt

EXPOSE 3111
RUN python /app/init_db.py
ENV FLASK_APP=app.py

CMD ["flask", "run", "--host=0.0.0.0", "--port=3111"]
