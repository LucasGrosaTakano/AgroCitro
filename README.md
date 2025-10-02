# AgroCitro

AgroCitro é um sistema web para gerenciamento de atividades agrícolas, incluindo plantio, irrigação e colheita. Ele permite o registro, consulta e agendamento dessas atividades, além de oferecer funcionalidades de autenticação de usuários.

## 📋 Funcionalidades

- **Plantio**: Registro e consulta de variedades plantadas.
- **Irrigação**: Agendamento e consulta de horários de irrigação.
- **Colheita**: Registro e consulta de colheitas realizadas.
- **Autenticação**: Cadastro e login de usuários.
- **Previsão Climática**: Exibição de dados climáticos para a cidade de Presidente Prudente.

---

## 🛠️ Configuração do Ambiente

### 1. **Pré-requisitos**
Certifique-se de ter as seguintes ferramentas instaladas:
- [Node.js](https://nodejs.org/) (versão 16 ou superior)
- [MySQL](https://www.mysql.com/) ou [MariaDB](https://mariadb.org/)
- [Git](https://git-scm.com/)

### 2. **Clone o Repositório**
git clone https://github.com/LucasGrosaTakano/AgroCitro
cd agrocitro

### 3. Instale as Dependências
Backend
```bash
cd database
npm install
```
Frontend e Servidor
```bash
cd ../js
npm install
```
### 4. Configuração do Banco de Dados
Acesse o MySQL/MariaDB:
```bash
mysql -u root -p
```
Execute o script SQL para criar o banco de dados e as tabelas:
```bash
SOURCE c:/Users/49084375807/Downloads/AgroCitro-main/database/AgroCitro_Banco (2).sq
```
Certifique-se de que o usuário citro_user tenha as permissões adequadas:
```bash
GRANT ALL PRIVILEGES ON agrocitro_bd.* TO 'citro_user'@'%' IDENTIFIED BY 'senhaforte123!';
FLUSH PRIVILEGES;
```

### 5. Configuração de Variáveis de Ambiente
Crie um arquivo .env na pasta js com as seguintes variáveis:
```bash
DB_HOST=10.111.9.90
DB_USER=citro_user
DB_PASSWORD=senhaforte123!
DB_NAME=agrocitro_bd
SERVER_PORT=3000
```

🚀 Execução do Projeto
#### 1. Inicie o Servidor
Na pasta js, execute:
```bash
npm start
```
O servidor estará disponível em: http://10.111.9.90:3000

#### 2. Acesse o Frontend
Abra o navegador e acesse:

Página de Login: http://10.111.9.90:3000/index.html
### 🧪 Testes e Validação
#### 1. Testar Funcionalidades
#### Cadastro de Usuário
Acesse a página de cadastro: http://10.111.9.90:3000/cadastrar.html

Preencha os campos e clique em "Cadastrar".

Verifique se o usuário foi salvo no banco de dados na tabela login.

#### Login

Acesse a página de login: http://10.111.9.90:3000/index.html

Insira as credenciais e clique em "Entrar".

Você será redirecionado para a página de plantio.

#### Registro de Plantio

Acesse a página de plantio: http://10.111.9.90:3000/plantio.html

Preencha o formulário e clique em "Registrar".

Verifique se o registro aparece na tabela e no banco de dados na tabela plantio.

#### Agendamento de Irrigação

Acesse a página de irrigação: http://10.111.9.90:3000/irrigacao.html

Preencha o formulário e clique em "Agendar".

Verifique se o agendamento aparece na tabela e no banco de dados na tabela irrigacao.

#### Registro de Colheita

Acesse a página de colheita: http://10.111.9.90:3000/colheita.html

Preencha o formulário e clique em "Registrar".

Verifique se o registro aparece na tabela e no banco de dados na tabela colheita.

#### Testar Previsão Climática
Acesse a página de irrigação: http://10.111.9.90:3000/irrigacao.html
Verifique se os dados climáticos são exibidos corretamente.
