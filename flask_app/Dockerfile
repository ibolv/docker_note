FROM ubuntu:latest
LABEL maintainer="Ivan <ivan@gmail.com>"
RUN apt-get update -y
RUN apt-get install -y python3-pip python3-dev build-essential python3-venv
RUN python3 -m venv /venv
COPY . /app
WORKDIR /app
RUN /venv/bin/pip install --no-cache-dir -r requirements.txt
ENV PATH="/venv/bin:$PATH"
CMD [ "python3", "app.py" ]