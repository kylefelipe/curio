# Curió - Formulários que cantam os dados do seu mapa

O Curió é um sistema de formulários que permite a criação de questionários e pesquisas de forma simples e intuitiva. Com ele, você pode coletar dados de forma eficiente e organizada, facilitando a análise posterior.

Um dos principais diferenciais do Curió é a sua capacidade de coletar dados geograficamente referenciados, permitindo que você visualize as respostas em um mapa. Isso é especialmente útil para pesquisas de campo, onde a localização das respostas é relevante bem como a utilização de softwares de geoprocessamento para análise dos dados.

## Instalação

O Curio é dividido em dois componentes principais: o backend, que é responsável por gerenciar os dados e a lógica do sistema, e o frontend, que é a interface do usuário. Para instalar o Curio, você precisará configurar ambos os componentes.

O primeiro passo é fazer o clone do repositório do Curio e instalar as dependências necessárias. O Curio utiliza o [Poetry](https://python-poetry.org/) para gerenciar as dependências do projeto, então você precisará instalá-lo antes de prosseguir.

```bash
git clone https://github.com/kylefelipe/curio.git
```

### Backend

O backend do Curio é construído com o framework [FastAPI](https://fastapi.tiangolo.com/) e utiliza um banco de dados [PostgreSQL](https://www.postgresql.org/) e [MongoDB](https://www.mongodb.com) para armazenar os dados. Ele utiliza o [Poetry](https://python-poetry.org/) para gerenciar as dependências do projeto.

Para instalar o backend, siga os passos abaixo:

1. Entre no diretório do backend:

    ```bash
    cd curio_backend
    ```

2. Instale as dependências do projeto:

    ```bash
    poetry install
    ```

3. Configure o banco de dados PostgreSQL e MongoDB. Você precisará criar um banco de dados para o Curio e configurar as variáveis de ambiente necessárias. Consulte o arquivo `.env.example` para ver as variáveis necessárias e crie um arquivo `.env` com as suas configurações.

4. Faça uma cópia do arquivo `.env.example` para `.env` e configure as variáveis de ambiente conforme necessário:

    ```bash
    cp .env.example .env
    ```

5. Inicie o servidor do backend:

    ```bash
    fastapi run
    ```

Para melhor documentação do backend, consulte [README.md](./curio_backend/README.md).

### Frontend

[Todo]

Criar a documentação do frontend, incluindo as dependências necessárias, como instalar e executar o frontend, e como integrá-lo com o backend.

### Docker

O Curio também pode ser executado usando Docker. Para isso, você precisará ter o [Docker](https://www.docker.com/) e o Docker compose instalado em sua máquina. Siga os passos abaixo para executar o Curio usando Docker:

1. Certifique-se de que o Docker e o Docker Compose estão instalados em sua máquina.

2. Navegue até o diretório raiz do Curio:

    ```bash
    cd curio
    ```

3. Execute o comando abaixo para iniciar os serviços do Curio:

    ```bash
    docker compose up --build
    ```

Isso irá construir as imagens necessárias e iniciar os containers do backend e do banco de dados. O Curio estará disponível em `http://localhost:8000`.

## Licença

O Curio é licenciado sob a [MIT License](./LICENSE). Sinta-se à vontade para usar, modificar e distribuir o código, desde que mantenha os créditos e a licença original.

## Contribuição

Se você deseja contribuir com o Curio, sinta-se à vontade para abrir uma issue ou pull request no repositório. Todas as contribuições são bem-vindas!
