FROM python:3.11.5

LABEL version="1.0"
LABEL maintainer="Yuto Chikazawa <chikazawa0517@gmail.com>"
LABEL description="vscode-state.vscdb-viewer"

ENV PYTHONUNBUFFERED=1

RUN apt-get update -y --fix-missing \
    && apt-get install -y --no-install-recommends \
    sudo \
    vim \
    git \
    make \
    curl \
    wget \
    less \
    locales

WORKDIR /usr/src/source

COPY ./source/requirements.txt  ./

RUN pip install --upgrade pip \
    && pip install -r requirements.txt

EXPOSE 8888

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--allow-root", "--NotebookApp.token="]
