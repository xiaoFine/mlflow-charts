FROM python:3.8
ARG version
RUN pip install mlflow==${version}

CMD [ "mlflow", "server" ]