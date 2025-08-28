# Repositório contendo todoo código da aplicação Webchat

Este projeto foi criado como requisito para uma das notas da disciplina Programação para Web 2, do curso Análise e Desenvolvimento de Sistemas do IFPB, campus Cajazeiras.

Aplicação consiste em um site/aplicativo web para troca de mensagens. Onde você pode criar sua conta e se comunicar com outros usuários online na rede.

 #### Repositórios originais:
 * **Front-end**: https://github.com/mikaelstl/pw2_exercise2_front/
 * **Back-end**: https://github.com/WarllaK/backend-chat

 #### Colaboradores
 * Mikael Stanley: [mikaelstl](https://github.com/mikaelstl/) - Front-end
 * Warlla Kelly: [WarllaK](https://github.com/WarllaK/) - Back-end
 * Bruno Henrique: [bruno-henr](https://github.com/bruno-henr/) - Integração entre back e front
 * Adrielly Ester: [adriellyEster](https://github.com/adriellyEster) - Refatoramento de código

A  aplicação foi construída com **Node.js** e **Express**, para o back-end, e **React** + **Vite** para o front-end, podendo ser executada facilmente com o **Yarn**/**NPM** e o **Docker**.

## Tecnologias Utilizadas

### Back-end
* **Node.js**: Ambiente de execução JavaScript.
* **Express**: Framework web para Node.js.
* **PostgreSQL**: Banco de dados relacional.
* **Prisma**: ORM moderno para interagir com o banco de dados.
* **WebSockets (lib `ws`)**: Para comunicação em tempo real entre os usuários.
* **JWT (JSON Web Tokens)**: Para autenticação e segurança das rotas.
* **Bcrypt**: Para criptografia de senhas.
* **Yarn**: Gerenciador de pacotes.

### Front-end
* **React.js**: Criação das telas e componentes principais.
* **Styled Components**: Biblioteca usada para criação do esqueleto de cada componente.
* **Vite**: Framework para facilitar a construção e configurações do React.
* **ContextApi**: Biblioteca para persistência de dados de usuário na aplicação.
* **ReactRouterDom**: Biblioteca que permite a navegação entre as páginas da aplicação.

---

##  Pré-requisitos


* [Node.js](https://nodejs.org/en/):20+
* [PostgreSQL](https://www.postgresql.org/) ou [Docker](https://www.docker.com/)
* [Yarn](https://yarnpkg.com/)(Opcional)


---

##  Iniciando o projeto

Com todos os requisitos instalados entre em cada repositório específico e rode os seguintes comandos:

```bash
npm install
```

#### Front-end
```bash
npm run dev
```

Acesse no seu navegador `http://localhost:5173`

#### Back-end

```bash
docker-compose up -d
npx prisma migrate dev --name init
npm start
```

O servidor estará rodando em `http://localhost:3000`.

---

#### Como usar

Será necessário dois computadores para testar a aplicação (Conectados na mesma rede).

1. Baixe o repositório do front-end em ambos os computadores, e o repositório do back-end somente em um deles.

2. Descubra o ip da máquina que executará o back-end:
```bash
ip -a
```
ou
```bash
ifconfig
```
Busque por algo como 192.168.0.X (X: número do seu computador na rede, varia de cada computador).

3. Troque onde aparece `localhost`, nos arquivos `/service/api.ts` e `/pages/Chat/index.tsx` pelo ip do computador onde está rodando o back-end.

4. Inicie tudo.

5. Acesse o `http://localhost:5173` em ambos os computadores.

6. Crie sua conta.

7. Agora basta acessar o chat e ao lado esquerdo estaram todos os usuários conectados, clique em um deles e troque mensagens.