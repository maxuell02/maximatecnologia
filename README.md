```bash
sudo apt -y update && apt -y upgrade
```

FAZENDO DOWNLOAD DO INSTALADOR & INICIANDO A PRIMEIRA INSTALAÇÃO (USAR SOMENTE PARA PRIMEIRA INSTALAÇÃO):

```bash
sudo apt install -y git && git clone https://github.com/maxuell02/maximatecnologia.git && sudo chmod -R 777 maximatecnologia && cd maximatecnologia && sudo ./install_primaria
```

ACESSANDO DIRETORIO DO INSTALADOR & INICIANDO INSTALAÇÕES ADICIONAIS (USAR ESTE COMANDO PARA SEGUNDA OU MAIS INSTALAÇÃO:
```bash
cd ./maximatecnologia && sudo ./install_instancia
```

********************Localhost**************************


OBS: Ter instalado o Banco de Dados, podendo usar o Xamp, o Wamp ou qualquer um de sua preferência.

================================================

Criar Banco de dados
CREATE DATABASE pressticket CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;

Clonar o repositório
git clone (seu projeto)

Entrar no diretório backend do King Ticket
cd SeuScript/backend

Criar o arquivo .env e inserir as informações do item 5

Editar os dados que serão inseridos no arquivo .env

NODE_ENV=  
BACKEND_URL=http://localhost  
FRONTEND_URL=http://localhost:3000  
PORT=8080  
PROXY_PORT=8080  
CHROME_BIN=C:\Program Files\Google\Chrome\Application\chrome.exe  

DB_DIALECT=mysql  
DB_HOST=localhost  
DB_TIMEZONE=-03:00  
DB_USER=root  
DB_PASS=  
DB_NAME=pressticket 

USER_LIMIT=3  
CONNECTIONS_LIMIT=1

JWT_SECRET=5g1yk7pD9q3YL0iBEuUlPwOiWLj3I5tK+/rhHm+jgdE=  
JWT_REFRESH_SECRET=F2c8gag5nvqQkBOmOu5dWkK+gqZnjPUzHmx7S2tWkvs=

Instalar as dependências
npm install

Buildar o projeto
npm run build

Criar as tabelas no banco de dados
npx sequelize db:migrate

Popular o banco de dados
npx sequelize db:seed:all

Rodar o servidor
npm start

Entrar no diretório frontend do King Ticket 
cd SeuScript/frontend
Criar o arquivo .env e inserir as informações do item 13

Editar os dados que serão inseridos no arquivo .env

REACT_APP_BACKEND_URL=http://localhost:8080
REACT_APP_HOURS_CLOSE_TICKETS_AUTO=

Instalar as dependências
npm install

Rodar o servidor
npm start

OBS: Caso ao rodar o frontend der erro de ssl, usar o comando abaixo no terminal.

set NODE_OPTIONS=--openssl-legancy-provider
==============================================================
