**Site Uniesp**
===============

Bem-vindo ao repositório do **Site Uniesp**, uma aplicação React desenvolvida com o objetivo de criar uma interface moderna e funcional para exibição de conteúdos institucionais e gerenciar notícias relacionadas à Faculdade UNIESP. Este projeto utiliza o JSON Server como backend fake para simular operações CRUD (Create, Read, Update, Delete).

* * * * *

**Funcionalidades**
-------------------

-   Exibição de páginas institucionais: "A Faculdade", "DPO e LGPD", entre outras.
-   Listagem, cadastro, edição e exclusão de notícias.
-   Layout responsivo com Material-UI.
-   Backend fake utilizando JSON Server para simulação de API REST.

* * * * *

**Tecnologias Utilizadas**
--------------------------

### **Frontend**

-   React (versão 18.x)
-   React Router DOM para navegação.
-   Material-UI (MUI) para componentes e estilização.
-   Axios para requisições HTTP.

### **Backend Fake**

-   JSON Server para simulação de uma API REST.

### **Build e Dev Server**

-   Vite para construção e servidor de desenvolvimento.

* * * * *

**Pré-requisitos**
------------------

Certifique-se de ter as seguintes ferramentas instaladas:

-   Node.js (versão 16 ou superior)
-   npm ou yarn

* * * * *

**Como Configurar o Projeto**
-----------------------------

### **1\. Clone o Repositório**

bash

Copiar código

`git clone https://github.com/seu-usuario/site-uniesp.git
cd site-uniesp`

### **2\. Instale as Dependências**

bash

Copiar código

`npm install`

### **3\. Configure o Backend Fake**

O backend fake utiliza o arquivo `data/db.json` como base de dados. Certifique-se de que ele está configurado corretamente:

json

Copiar código

`{
  "noticias": [
    {
      "id": "1",
      "titulo": "Avanços na energia limpa revolucionam o setor",
      "texto": "Novas tecnologias em energia renovável estão transformando o mercado global, com investimentos recordes em projetos de sustentabilidade.",
      "imagem": "/imagens/energia-limpa.jpg"
    }
  ]
}`

### **4\. Inicie o Backend Fake**

Execute o JSON Server para servir os dados do arquivo `db.json`:

bash

Copiar código

`npm run server`

O JSON Server estará disponível em: `http://localhost:3000`.

### **5\. Inicie o Frontend**

Inicie o servidor de desenvolvimento do Vite:

bash

Copiar código

`npm run dev`

O site estará disponível em: `http://localhost:5173`.

* * * * *

**Scripts Disponíveis**
-----------------------

No diretório do projeto, você pode executar os seguintes comandos:

-   **`npm run dev`**: Inicia o servidor de desenvolvimento (frontend).
-   **`npm run build`**: Gera o build de produção.
-   **`npm run preview`**: Pré-visualiza o build.
-   **`npm run server`**: Inicia o JSON Server (backend fake).

* * * * *

**Estrutura do Projeto**
------------------------

csharp

Copiar código

`site-uniesp/
├── public/              # Arquivos públicos (favicon, imagens)
├── src/                 # Código fonte do frontend
│   ├── components/      # Componentes reutilizáveis (Navbar, BannerAd)
│   ├── pages/           # Páginas principais do site
│   ├── styles/          # Estilos globais ou específicos (opcional)
│   ├── App.jsx          # Componente principal
│   ├── main.jsx         # Ponto de entrada do React
├── data/                # Arquivo de dados para o JSON Server
│   └── db.json          # Base de dados fake
├── package.json         # Configurações e dependências do projeto
└── vite.config.js       # Configuração do Vite`

* * * * *

**Rotas do Backend Fake**
-------------------------

O JSON Server cria automaticamente as seguintes rotas:

-   **`GET /noticias`**: Lista todas as notícias.
-   **`GET /noticias/:id`**: Busca uma notícia específica.
-   **`POST /noticias`**: Adiciona uma nova notícia.
-   **`PUT /noticias/:id`**: Atualiza uma notícia existente.
-   **`DELETE /noticias/:id`**: Remove uma notícia.

* * * * *

**Contribuição**
----------------

Sinta-se à vontade para contribuir com melhorias! Siga os passos abaixo:

1.  Faça um fork do repositório.
2.  Crie uma branch com a feature ou correção:

    bash

    Copiar código

    `git checkout -b minha-feature`

3.  Faça o commit das alterações:

    bash

    Copiar código

    `git commit -m "Descrição da minha feature"`

4.  Envie as alterações:

    bash

    Copiar código

    `git push origin minha-feature`

5.  Abra um Pull Request.

* * * * *

**Licença**
-----------

Este projeto é distribuído sob a licença **MIT**.