FROM python:3.7.9-slim-stretch

ENV LANG=C.UTF-8
ENV PYPI_CLIBOA_VERSION=1.3.5b0
ENV PATH=$PATH:/home/cliboa/.local/bin

RUN adduser cliboa --disabled-password
USER cliboa

RUN pip install --user \
      cliboa=="${PYPI_CLIBOA_VERSION}"

RUN cliboadmin init /home/cliboa/myproject
WORKDIR /home/cliboa/myproject
RUN pip install -r requirements.txt
RUN cliboadmin create myetl

COPY conf conf
COPY bin /home/cliboa/.local/bin

CMD [ "cliboa", "-h" ]
