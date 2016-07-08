FROM debian:squeeze

# repos already expired
ENV APT_HACK="-o Acquire::Check-Valid-Until=false"

# and placed in debian archives
COPY sources.list /etc/apt/sources.list

RUN apt-get ${APT_HACK} update \
    && apt-get install -y --no-install-recommends \
        build-essential \
        python-setuptools \
        python-dev \
        libssl-dev \
        libffi-dev \
    && easy_install pip \
    && pip install -U setuptools \
    && pip install -U wheel \
    && pip install \
        `# common ansible` \
        pycrypto \
        cryptography \
        jinja2 \
        paramiko \
        PyYAML \
    && rm -rf /var/lib/apt/lists/* /root/.cache
