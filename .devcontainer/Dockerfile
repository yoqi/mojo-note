
FROM mcr.microsoft.com/devcontainers/universal:2

ARG DEFAUL_TZ=America/Los_Angeles
ENV DEFAULT_TZ=$DEFAULT_TZ

ARG AUTH_KEY=DEFAULT_KEY
ENV AUTH_KEY=$AUTH_KEY

RUN curl https://get.modular.com | MODULAR_AUTH=$AUTH_KEY sh - \
    && modular install mojo

ARG MODULAR_HOME="/root/.modular"
ENV MODULAR_HOME=$MODULAR_HOME
ENV PATH="$PATH:$MODULAR_HOME/pkg/packages.modular.com_mojo/bin"

# RUN conda init 
# RUN jupyter labextension disable "@jupyterlab/apputils-extension:announcements"
# CMD ["jupyter", "lab", "--ip='*'", "--NotebookApp.token=''", "--NotebookApp.password=''","--allow-root"]
