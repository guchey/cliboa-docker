FROM python:3.7

ENV LANG C.UTF-8
ENV PYPI_PIPENV_VERSION=2018.11.26
ENV PYPI_CLIBOA_VERSION=1.3.2b0

RUN pip install \
      pipenv=="${PYPI_PIPENV_VERSION}" \
      cliboa=="${PYPI_CLIBOA_VERSION}"
RUN cliboadmin init cliboa
WORKDIR /cliboa
COPY conf conf
RUN rm common/scenario.yml
RUN pipenv install --system --skip-lock
RUN cliboadmin create default

COPY bin/cliboa /usr/local/bin/cliboa
RUN chmod +x /usr/local/bin/cliboa

CMD [ "cliboa", "-h" ]