🇦🇴 Angola Tourism Insight

O Angola Tourism Insight é uma plataforma digital de análise e previsão de dados turísticos de Angola, desenvolvida para utilizar dados históricos e variáveis relacionadas ao turismo para gerar previsões e informações que apoiem a tomada de decisões.

O projeto integra uma aplicação web desenvolvida com Laravel e uma API em Python, responsável pela utilização do modelo de Machine Learning para realizar previsões.

O projeto foi desenvolvido no contexto de um projeto Capstone pela equipe formada por:

Ângelo Rocha Garcia
Azevaldo Miguel Caluaco
Dorivaldo Catala Mandele
Francisco Ramos Cadete
Francisco Benguela José
Reinaldo Sagrado Paulo
🎯 Objetivo

O objetivo do Angola Tourism Insight é utilizar dados turísticos e ambientais para identificar padrões e realizar previsões sobre o fluxo de turistas em Angola.

A plataforma procura transformar dados históricos em informações úteis para apoiar gestores, empresas e outros interessados no planejamento turístico.

Entre os objetivos definidos para o projeto estão:

Identificar padrões no comportamento turístico em Angola.
Prever fluxos turísticos com base em diferentes variáveis.
Disponibilizar informações e previsões através de uma plataforma web.
Apoiar decisões relacionadas ao planejamento turístico.
Promover uma abordagem baseada em dados para o desenvolvimento do turismo.

O projeto também está relacionado aos Objetivos de Desenvolvimento Sustentável, especialmente aos ODS 8, 9 e 11.

🧠 Machine Learning

A previsão é realizada através de um modelo de Machine Learning desenvolvido em Python.

O projeto considera variáveis relacionadas ao fluxo turístico e às condições que podem influenciar o número de visitantes, como:

Dados históricos de turistas.
Localidade.
Período.
Temperatura.
Precipitação.
Eventos.
Feriados.
Sazonalidade.

A documentação do projeto prevê a utilização de algoritmos como Random Forest, Regressão Linear, Regressão Ridge e Redes Neurais para a modelagem preditiva.

📊 Principais funcionalidades
🔮 Previsão de turistas

A funcionalidade principal da plataforma é a previsão do número de turistas para determinada localidade e período.

Os resultados podem ser classificados em três níveis:

Pico: fluxo turístico elevado.
Médio: fluxo turístico dentro de uma faixa intermediária.
Baixo: fluxo turístico reduzido.

Essa classificação é baseada na análise estatística dos dados históricos por região.

💡 Sugestões inteligentes

A plataforma pode gerar sugestões com base nos resultados das previsões:

Sugestão de Pico.
Sugestão Média.
Sugestão Baixa.

Essas sugestões procuram auxiliar na interpretação dos resultados e no planejamento de ações relacionadas ao turismo.

📁 Gestão de arquivos e publicações

A plataforma possui um módulo para gestão de documentos e arquivos relacionados ao turismo.

Podem ser disponibilizados:

Relatórios turísticos.
Estudos.
Dados estatísticos.
Documentos técnicos.
Outros documentos relacionados ao setor.

Os arquivos podem passar por diferentes estados, como:

Pendente.
Aprovado.
Arquivado.

Os documentos aprovados podem ser disponibilizados na área pública da plataforma.

📈 Histórico e informações

A plataforma mantém informações relacionadas às previsões e aos documentos, permitindo acompanhar dados como:

Data de criação.
Data de atualização.
Usuário responsável.
Tipo de arquivo.
Estado de aprovação.
Histórico das operações.
👥 Tipos de utilizadores

A plataforma possui diferentes níveis de acesso.

Administrador

Possui o maior nível de acesso ao sistema.

É responsável pela administração geral da plataforma, incluindo gerenciamento de utilizadores, documentos, previsões, permissões e configurações.

Gestor

Atua no nível operacional e pode trabalhar com previsões e informações relacionadas à sua província.

Pode consultar históricos e utilizar os resultados das previsões para apoiar análises e recomendações locais.

Prestador

Responsável principalmente pelo envio de dados e documentos para a plataforma.

Pode gerenciar os seus próprios arquivos de acordo com as regras de publicação do sistema.

A definição desses papéis e respectivas permissões está descrita na documentação funcional do projeto.

🏗️ Arquitetura do projeto

O projeto está dividido em diferentes componentes:

Angola-Tourism-Insight/
│
├── api-modelo/
│   ├── README.md
│   ├── index.py
│   ├── modelo_prev-turista.joblib
│   └── requirements.txt
│
├── docs/
│   ├── ideação.pdf
│   ├── Refinamento do modelo.pdf
│   ├── Nota Conceitual e Plano de Implementação.pdf
│   ├── Implantação Deployment.pdf
│   └── Preparação dos dados e engenharia.pdf
│
├── laravel-app/
│   └── README.md
│
├── notebooks/
│   └── 001.ipynb
│
├── turistas3.sql
│
└── README.md
api-modelo/

Contém a API Python utilizada para disponibilizar o modelo de Machine Learning.

laravel-app/

Contém a aplicação web desenvolvida com Laravel.

notebooks/

Contém notebooks utilizados durante o desenvolvimento e análise do projeto.

docs/

Contém a documentação produzida durante as diferentes etapas do projeto.

turistas3.sql

Arquivo de backup da base de dados MySQL utilizada pela aplicação.

🛠️ Tecnologias
Aplicação web
PHP
Laravel
HTML5
CSS
JavaScript
Bootstrap
API e Machine Learning
Python
Scikit-learn
Pandas
NumPy
Joblib

A documentação do projeto também registra o uso de ferramentas como Jupyter Notebook, TensorFlow, Matplotlib, Plotly e Streamlit no desenvolvimento da solução de dados e Machine Learning.

⚙️ Instalação e execução

O projeto possui duas partes que precisam ser configuradas:

API Python
Aplicação Laravel
1. Executar a API Python

Entre na pasta:

cd api-modelo

Instale as dependências:

pip install -r requirements.txt

Execute a API através do arquivo:

python index.py

A API deve permanecer em execução enquanto a aplicação Laravel estiver sendo utilizada.

2. Configurar a aplicação Laravel

Em outro terminal, entre na pasta:

cd laravel-app

Instale as dependências:

composer install

Gere a chave da aplicação:

php artisan key:generate

Configure o arquivo .env com os dados de conexão do MySQL.

A base de dados utilizada pelo projeto é:

turistas3

O arquivo turistas3.sql, localizado na raiz do repositório, deve ser importado no MySQL.

Depois da configuração do banco, execute:

php artisan serve

A aplicação poderá ser acessada através do endereço disponibilizado pelo Laravel.

Importante: é necessária uma conexão com a Internet para utilizar o projeto.

🔐 Contas de acesso

O projeto possui contas de demonstração para diferentes perfis e províncias.

Perfil	E-mail	Senha
Administrador	admin@gmail.com	password
Luanda	luanda@gmail.com	123456789
Benguela	benguela@gmail.com	123456789
Huíla	huila@gmail.com	123456789

Atenção: estas credenciais são as fornecidas na documentação do projeto. Se forem credenciais reais utilizadas fora de um ambiente de demonstração, não devem ser mantidas publicamente no README.

📚 Documentação

A pasta docs/ contém os documentos produzidos durante o desenvolvimento do projeto, incluindo documentação sobre:

Ideação.
Preparação dos dados.
Engenharia de recursos.
Refinamento do modelo.
Plano de implementação.
Implantação e deployment.
📄 Documentação específica

Para informações sobre a aplicação Laravel:

👉 README da aplicação Laravel

Para informações sobre a API Python:

👉 README da API Python

🌱 Objetivos de Desenvolvimento Sustentável

O projeto está relacionado aos seguintes ODS:

ODS 8 — Trabalho Decente e Crescimento Económico
ODS 9 — Indústria, Inovação e Infraestrutura
ODS 11 — Cidades e Comunidades Sustentáveis

A proposta do projeto relaciona análise de dados, previsão turística e desenvolvimento sustentável.

👨‍💻 Equipe
Ângelo Rocha Garcia
Azevaldo Miguel Caluaco
Dorivaldo Catala Mandele
Francisco Ramos Cadete
Francisco Benguela José
Reinaldo Sagrado Paulo

Angola Tourism Insight
Plataforma de análise e previsão do fluxo turístico em Angola.
