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
-   npm

* * * * *

**Como Configurar o Projeto**
-----------------------------

### **1\. Clone o Repositório**

bash

    git clone https://github.com/WaldirPontualFilho/site_uniesp.git
    cd site-uniesp

### **2\. Instale as Dependências**

bash

    npm install

### **3\. Configure o Backend Fake**

O backend fake utiliza o arquivo `data/db.json` como base de dados. Certifique-se de que ele está configurado corretamente:

json

    {
        "noticias": [
        {
          "id": "1",
          "titulo": "Avanços na energia limpa revolucionam o setor",
          "texto": "Novas tecnologias em energia renovável estão transformando o mercado global, com investimentos recordes em projetos de sustentabilidade.",
          "imagem": "/imagens/energia-limpa.jpg"
        }
      ]
    }

### **4\. Inicie o Backend Fake**

Execute o JSON Server para servir os dados do arquivo `db.json`:

bash

    npm run server

O JSON Server estará disponível em: `http://localhost:3000`.

### **5\. Inicie o Frontend**

Inicie o servidor de desenvolvimento do Vite:

bash

    npm run dev

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

    site-uniesp/
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
    └── vite.config.js       # Configuração do Vite

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

## **Detalhes das Tecnologias**


### **React Router DOM**

O **React Router DOM** é utilizado neste projeto para criar uma navegação fluida entre as páginas do site. Cada página, como "A Faculdade", "DPO e LGPD" e "Notícias", está vinculada a uma rota específica. Ele permite:

- Navegação declarativa por meio de componentes como `<Routes>` e `<Route>`.
- Controle de rotas dinâmicas para manipulação de conteúdo com base em parâmetros (e.g., `/noticias/:id`).
- Navegação programática para redirecionar usuários após ações específicas, como salvar ou editar uma notícia.

### **Axios**

O **Axios** é uma biblioteca para realizar requisições HTTP e facilita a comunicação entre o frontend e o backend fake (JSON Server). Neste projeto, o Axios é utilizado para:

- Buscar dados das notícias (GET).
- Enviar novas notícias para o backend (POST).
- Atualizar notícias existentes (PUT).
- Excluir notícias (DELETE).

Os endpoints são definidos dinamicamente, tornando o código modular e reutilizável.

### **Material-UI (MUI)**

O **Material-UI** (MUI) é usado para criar um layout moderno e responsivo. Com seus componentes pré-construídos e temas personalizáveis, o MUI permite:

- Criação de botões, cards, grids e formulários estilizados de maneira consistente.
- Implementação de responsividade com o sistema de `Grid`.
- Personalização do tema para seguir a identidade visual do projeto.

Exemplo de um **Card** utilizando o MUI:


    import { Card, CardContent, Typography } from '@mui/material';
    
    const NoticiaCard = ({ titulo, texto }) => (
      <Card sx={{ maxWidth: 345, margin: 'auto' }}>
        <CardContent>
          <Typography variant="h5" component="div">
            {titulo}
          </Typography>
          <Typography variant="body2" color="text.secondary">
            {texto}
          </Typography>
        </CardContent>
      </Card>
    );
    
    export default NoticiaCard;


**Contribuição**
----------------

Sinta-se à vontade para contribuir com melhorias! Siga os passos abaixo:

1.  Faça um fork do repositório.
2.  Crie uma branch com a feature ou correção:

    bash
    `git checkout -b minha-feature`

3.  Faça o commit das alterações:

    bash
   `git commit -m "Descrição da minha feature"`

4.  Envie as alterações:

    bash
    `git push origin minha-feature`

6.  Abra um Pull Request.

* * * * *

**Licença**
-----------

Este projeto é distribuído sob a licença **MIT**.
