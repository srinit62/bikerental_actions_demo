FROM python:3.12

RUN mkdir /bike_sharing_api
RUN mkdir /bike_sharing_api/app
RUN mkdir /bike_sharing_api/app/schemas

WORKDIR /bike_sharing_api

copy bike_sharing_api/bikeshare_model-0.0.1-py3-none-any.whl /bike_sharing_api
copy bike_sharing_api/app/*.py /bike_sharing_api/app/
copy bike_sharing_api/app/schemas/*.py /bike_sharing_api/app/schemas/

copy bike_sharing_api/requirements.txt /bike_sharing_api/

# Install the application dependencies
RUN pip install -r /bike_sharing_api/requirements.txt

# Setup an app user so the container doesn't run as the root user
#RUN useradd app
#USER app

CMD ["python", "app/main.py"]

