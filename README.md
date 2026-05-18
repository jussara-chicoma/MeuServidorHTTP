# MeuServidorHTTP
Este projeto é um servidor HTTP desenvolvido em GoLang que permite realizar o cadastro de agendamento, utilizando as configurações basicas do CRUD (Criar, Ler, Atualizar e Excluir). 
_________________________________________________________________________________________________________________________________________________________________________
**PASSOS PARA CONFIGURAÇÃO**
Clone o repositório:

git clone <URL_DO_REPOSITORIO>
cd servidorHTTP

**Configure o arquivo .env: Crie um arquivo .env na raiz do projeto com as seguintes variáveis:**

DB_USER=<seu_usuario>
DB_PASSWORD=<sua_senha>
DB_NAME=<nome_do_banco>
DB_HOST=<host_do_banco>
DB_PORT=<porta_do_banco>
Configuração do Banco de Dados:


**Crie a tabela de usuários no banco de dados com o seguinte comando SQL:**
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    born_date DATE NOT NULL,
    password VARCHAR(300) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
Instale as dependências: Execute o comando abaixo para instalar as dependências do projeto:

go mod tidy
