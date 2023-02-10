FROM python:3.10


COPY ./DJ-4hw_M2M-relations /src/DJ-4hw_M2M-relations

WORKDIR /src/DJ-4hw_M2M-relations

RUN pip install -r requirements.txt

ENV SECRET_KEY="nt7n&7df*ik63*7&&0g)%ctpav$=ovj2ab(%271d@ehebs4tp+"
ENV DEBUG="True"
ENV ALLOWED_HOSTS="127.0.0.1,localhost"

RUN python manage.py migrate

RUN python manage.py loaddata articles.json

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]