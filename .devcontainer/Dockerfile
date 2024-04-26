ARG VARIANT="3"
FROM mcr.microsoft.com/vscode/devcontainers/python:${VARIANT}


USER ${USER}
ARG HOME="/home/${USER}"
WORKDIR ${HOME}

# Set up Python environment
ARG PYTHON_VERSION=3.9
ENV PYENV_ROOT=${HOME}/.pyenv
ARG PYENV_PATH="${PYENV_ROOT}/bin:${PYENV_ROOT}/shims"
ARG PDM_PATH="${HOME}/.local/bin"
ENV PATH="${PYENV_PATH}:${PDM_PATH}:$PATH"
RUN curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash \
    && echo 'eval "$(pyenv init -)"' >> ${HOME}/.bashrc \
    && pyenv install -v ${PYTHON_VERSION} \
    && pyenv global ${PYTHON_VERSION}

# Install Python packages from requirements.txt
COPY requirements.txt /tmp/
RUN pip install -r /tmp/requirements.txt