FROM homeassistant/home-assistant:beta

COPY . /entry/requirements

WORKDIR /entry

RUN \
  python3 -m pip --disable-pip-version-check install -U \
    setuptools \
    pip \
  && python3 -m pip install \
    pipdeptree==1.0.0 \
    stdlib-list==0.7.0 \
    tqdm

ENTRYPOINT ["python3", "-m", "requirements"]