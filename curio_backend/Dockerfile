FROM python:3.12.1-slim

# Instala dependências do sistema
RUN apt-get update && apt-get install -y \
  build-essential curl libpq-dev gcc \
  && apt-get clean && rm -rf /var/lib/apt/lists/*

# Instala o Poetry
ENV POETRY_VERSION=2.1.2
RUN curl -sSL https://install.python-poetry.org | python3 -
ENV PATH="/root/.local/bin:$PATH"

# Criando o venv fora de /app

ENV VIRTUAL_ENV=/opt/.venv
RUN python3 -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

# Cria pasta de trabalho
WORKDIR /app/

# Copia só os arquivos de dependência primeiro
COPY pyproject.toml poetry.lock* /app/

# Instala dependências do projeto (sem virtualenv)
RUN poetry config virtualenvs.create false
RUN poetry install --no-interaction --no-ansi --no-root

# Copia o restante da aplicação
COPY . /app/

# Exponha a porta da API
EXPOSE 8000

# Comando final (AQUI ESTAVA O ERRO)
CMD ["poetry", "run", "uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
