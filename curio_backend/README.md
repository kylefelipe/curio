# Curio Backend - Backend do Curió, um sistema de formulários que canta os dados do seu mapa

Curió Backend é um backend desenvolvido com FastAPI, destinado a fornecer uma API robusta para o Curió, um sistema de formulários que transforma dados geográficos em informações úteis e acessíveis. Este repositório contém a implementação do backend, incluindo rotas de autenticação, gerenciamento de usuários e integração com banco de dados PostgreSQL.

Este repositório utiliza [Poetry](https://python-poetry.org/) para gerenciamento de dependências e ambiente virtual

## Dependências

Para instalar as dependências do projeto, execute o seguinte comando:

```bash
poetry install
```

## Configuração do Ambiente

Copie o arquivo `.env.example` para `.env` e configure as variáveis de ambiente conforme necessário. As variáveis de ambiente são usadas para configurar a conexão com o banco de dados e outras configurações do aplicativo.

```bash

cp .env.example .env
```

## Execução do Servidor

Para iniciar o servidor de desenvolvimento, execute o seguinte comando:

```bash
fastapi run
```

## Testes

Instale as dependencias de desenvolvimento com o seguinte comando:

```bash
poetry install --with dev
```

Para executar os testes, utilize o seguinte comando:

```bash
pytest
```

## Documentação da API

O sistema disponibiliza um swagger para a documentação da API. Você pode acessá-lo em:

[http://localhost:8000/docs](http://localhost:8000/docs)

E também uma versão alternativa com redoc:

[http://localhost:8000/redoc](http://localhost:8000/redoc)

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests para melhorias, correções de bugs ou novas funcionalidades.

## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
