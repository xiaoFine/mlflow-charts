FROM python:3.8
ARG version
RUN pip install "mlflow[extras]==${version}" mlflow-skinny sqlalchemy alembic sqlparse \
    -i https://pypi.doubanio.com/simple
CMD [ "mlflow", "server" ]