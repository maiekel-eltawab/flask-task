FROM ubuntu:latest

RUN apt update && \
    apt install -y python3 python3-pip build-essential gcc libffi-dev libssl-dev && \
    rm -rf /var/lib/apt/lists/

WORKDIR /app

COPY . /app

RUN pip3 install --no-cache-dir --break-system-packages -r requirements.txt

EXPOSE 5000

CMD ["flask","run","--host=0.0.0.0"]

