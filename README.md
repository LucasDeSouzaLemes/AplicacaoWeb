# Sistema de Pesquisa de Satisfação

Este projeto foi desenvolvido para criar uma aplicação web para coletar pesquisas de satisfação dos alunos do Curso de Análise e Desenvolvimento de Sistemas. A aplicação utiliza Docker para fornecer um ambiente de desenvolvimento consistente e portátil.


## Estrutura do Projeto

AplicacaoWeb<br>
├── MongoDB<br>
│ ├── dockerfile<br>
│ ├── README.md<br>
│ └── Unifaat.md<br>
├── Nodejs<br>
│ └── dockerfile<br>
├── PostgreSQL<br>
│ └── dockerfile<br>
├── docker-compose.yml<br>
└── Readme.md<br>
## Como Rodar o Docker-Compose


Para rodar o projeto utilizando o Docker-Compose, siga os passos abaixo:

1. Clone o Repositório:
   ```bash
   git clone <repository-url>
   cd AplicacaoWeb
   ```

2. Certifique-se de que você tem o Docker e o Docker-Compose instalados na sua máquina:

```bash
docker --version
docker-compose --version
```
3. No diretório raiz do projeto, execute o seguinte comando para parar e remover quaisquer contêineres existentes:

```bash
docker-compose down
```
4. Remova o volume de dados do PostgreSQL (se necessário):

```bash
docker volume rm AulaMicroservico_postgres_data
```

5. Execute o comando para iniciar os contêineres com o Docker-Compose:

```bash
docker-compose up --build
```

6. Assim que os containers estiverem em execução, você pode acessar a aplicação em `http://localhost:3000`.

## O projeto consiste nos seguintes componentes principais:

- **Containers Docker**:
  - **MongoDB**: Um banco de dados NoSQL para armazenamento de dados mais flexíveis.
  - **Node.js**: O servidor da aplicação que executa a aplicação de pesquisa de satisfação.
  - **PostgreSQL**: Um banco de dados relacional para armazenar dados estruturados.

- **Código Fonte**:
  - O código da aplicação está localizado no diretório `src`, que inclui o arquivo principal da aplicação (`app.js`) e o `package.json` para gerenciar as dependências.



## Configuração

- **PostgreSQL**: : O container do PostgreSQL está configurado com acesso administrativo. Você pode personalizar as configurações do banco de dados no arquivo `AplicacaoWeb/postgres/Dockerfile`.

- **MongoDB**: O container do MongoDB também está configurado com acesso administrativo. A configuração pode ser ajustada no arquivo `AplicacaoWeb/mongodb/Dockerfile`.

- **Node.js**: O container do Node.js executa a versão 22 e está configurado no arquivo `AplicacaoWeb/nodejs/Dockerfile`.

## Observações

* Personalize as configurações no arquivo docker-compose.yml conforme necessário.
