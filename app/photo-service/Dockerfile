FROM python:3.8
WORKDIR "/code"
COPY ./requirements.txt /code/requirements.txt
RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt
#RUN python -m pip install grpcio
#RUN python -m pip install grpcio-tools
#RUN pip install mongoengine Pillow python-multipart
COPY ./*.py /code/
ENV GRACEFUL_TIMEOUT=10
ENV MONGO_HOST 172.17.0.2
CMD ["uvicorn", "photo_service:app", "--host", "0.0.0.0", "--port", "80"]
