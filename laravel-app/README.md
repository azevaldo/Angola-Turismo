Angola Tourism Insight — Laravel

Esta pasta contém a aplicação web do Angola Tourism Insight, desenvolvida com Laravel.

A aplicação funciona como a interface web do projeto e utiliza uma API desenvolvida em Python para realizar previsões através do modelo de Machine Learning.

Para conhecer o projeto completo, sua arquitetura, objetivos e documentação, consulte o README principal.

🛠️ Tecnologias
PHP
Laravel
HTML5
CSS
JavaScript
Bootstrap
MySQL
📋 Requisitos

Antes de executar a aplicação, certifique-se de possuir:

PHP
Composer
MySQL ou MariaDB
Laravel
A API Python do projeto configurada e em execução
📥 Instalação
1. Entrar na aplicação

A partir da raiz do projeto:

cd laravel-app
2. Instalar as dependências
composer install
3. Configurar o arquivo .env

Crie o arquivo .env a partir do .env.example:

cp .env.example .env

No Windows, também é possível criar o .env manualmente a partir do .env.example.

Configure as informações de conexão com o banco de dados.

O projeto utiliza o banco:

turistas3

Exemplo:

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=turistas3
DB_USERNAME=root
DB_PASSWORD=

Ajuste o usuário e a senha conforme a configuração do seu ambiente.

4. Gerar a chave da aplicação
php artisan key:generate
5. Importar a base de dados

Na raiz do repositório existe o arquivo:

turistas3.sql

Importe esse arquivo no MySQL/MariaDB.

Depois, confirme se o nome configurado no .env corresponde ao banco importado:

DB_DATABASE=turistas3

A base de dados já está disponibilizada no projeto. Portanto, ao utilizar o arquivo turistas3.sql, não é necessário criar a estrutura do banco manualmente através das migrations.

🤖 API Python

A aplicação Laravel depende da API Python responsável pelo modelo de Machine Learning.

Antes de utilizar as funcionalidades que dependem da previsão, entre na pasta:

cd ../api-modelo

Instale as dependências:

pip install -r requirements.txt

Execute a API:

python index.py

Mantenha a API em execução enquanto estiver utilizando a aplicação Laravel.

Depois, em outro terminal, volte para a aplicação:

cd ../laravel-app
▶️ Executar a aplicação

Com o banco configurado e a API Python em execução:

php artisan serve

A aplicação poderá ser acessada pelo endereço fornecido pelo Laravel, normalmente:

http://127.0.0.1:8000
🔐 Contas de acesso

Para testes, o projeto possui as seguintes contas:

Perfil	E-mail	Senha
Administrador	admin@gmail.com	password
Utilizador de Luanda	luanda@gmail.com	123456789
Utilizador de Benguela	benguela@gmail.com	123456789
Utilizador de Huíla	huila@gmail.com	123456789

Essas contas permitem testar os diferentes níveis de acesso disponíveis na aplicação.

Nota de segurança: as credenciais acima devem ser utilizadas apenas em ambiente de demonstração. Não utilize senhas reais em um repositório público.

🏗️ Estrutura principal
laravel-app/
│
├── app/
├── bootstrap/
├── config/
├── database/
├── public/
├── resources/
├── routes/
├── storage/
├── artisan
├── composer.json
└── .env
app/

Contém a lógica principal da aplicação Laravel.

database/

Contém os recursos relacionados à base de dados, incluindo migrations e seeders existentes no projeto.

resources/

Contém os recursos da interface da aplicação.

routes/

Contém as rotas utilizadas pela aplicação.

public/

Contém os arquivos públicos da aplicação.

🧠 Integração com o modelo

A aplicação Laravel utiliza a API Python para acessar o modelo de Machine Learning.

O fluxo geral é:

Utilizador
    │
    ▼
Aplicação Laravel
    │
    ▼
API Python
    │
    ▼
Modelo de Machine Learning
    │
    ▼
Previsão
    │
    ▼
Aplicação Laravel
    │
    ▼
Resultado apresentado ao utilizador

A API e o modelo são mantidos separadamente da aplicação Laravel, permitindo que a camada web e a camada de Machine Learning sejam desenvolvidas de forma independente.

📚 Documentação

A documentação completa do projeto está disponível na pasta docs/ localizada na raiz do repositório.

Entre os documentos estão materiais relacionados a:

Ideação.
Preparação dos dados.
Engenharia de recursos.
Refinamento do modelo.
Plano de implementação.
Implantação e deployment.
🔙 Voltar para o projeto



Angola Tourism Insight — Laravel Application

Desenvolvido pela equipe do projeto Angola Tourism Insight.
