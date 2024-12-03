# Documentação do Projeto: Ristorante Delicias Real

Este projeto é um aplicativo React que exibe um menu de pratos com seus detalhes e comentários. Ele foi desenvolvido como parte de um exercício para consolidar conceitos de React, incluindo componentes, estado e Bootstrap.

---

## **Estrutura do Projeto**

O projeto é composto pelos seguintes arquivos principais:

### 1. **`App.js`**
- **Função Principal**: Controla a estrutura principal do aplicativo e gerencia os dados.
- **Componentes Utilizados**:
  - `Navbar`: Exibe o nome do restaurante e informações do aluno.
  - `Menu`: Renderiza o menu com os pratos disponíveis.
- **Estado**:
  - `dishes`: Gerencia a lista de pratos importada do arquivo `dishes.js`.

---

### 2. **`MenuComponent.js`**
- **Função Principal**: Exibe uma lista de pratos disponíveis e permite selecionar um prato para exibir seus detalhes.
- **Estado**:
  - `selectedDish`: Gerencia o prato atualmente selecionado.
- **Componentes Utilizados**:
  - `DishDetail`: Exibe os detalhes do prato selecionado.
- **Estilização**:
  - Utiliza classes do Bootstrap para responsividade (`col-12`, `col-md-5`, `m-1`).

---

### 3. **`DishdetailComponent.js`**
- **Função Principal**: Renderiza os detalhes do prato selecionado e sua lista de comentários.
- **Funções**:
  - `renderDish`: Renderiza os detalhes do prato em um `Card`.
  - `renderComments`: Exibe os comentários do prato em uma lista não estilizada.
- **Comportamento**:
  - Se o prato for `null`, retorna um elemento vazio.
- **Estilização**:
  - Usa componentes do Reactstrap (`Card`, `CardImg`, `CardBody`, `CardTitle`, `CardText`).
  - Responsividade garantida com classes do Bootstrap.

---

### 4. **`dishes.js`**
- **Função Principal**: Contém os dados dos pratos e seus comentários.
- **Estrutura**:
  Cada prato é representado por um objeto com as seguintes propriedades:
  - `id`: Identificador único do prato.
  - `name`: Nome do prato.
  - `image`: Caminho para a imagem do prato.
  - `category`, `label`, `price`: Informações adicionais.
  - `description`: Descrição detalhada do prato.
  - `comments`: Lista de comentários associados ao prato, incluindo:
    - `id`: Identificador único do comentário.
    - `comment`: Texto do comentário.
    - `author`: Autor do comentário.
    - `date`: Data do comentário.

---

## **Requisitos Implementados**

### Tarefa 1: Adicionar o `DishdetailComponent`
- Substituímos o cartão no `MenuComponent` pelo novo componente `DishdetailComponent`.
- Passamos as informações do prato selecionado como `props` para o `DishDetail`.
- Configuramos a responsividade com classes do Bootstrap.

### Tarefa 2: Detalhes do Prato
- Criamos a função `renderDish` para exibir os detalhes do prato selecionado.
- Utilizamos o componente `Card` do Reactstrap para estilizar a exibição.

### Tarefa 3: Lista de Comentários
- Criamos a função `renderComments` para renderizar os comentários em uma lista não estilizada.
- Incluímos o nome do autor e a data formatada de cada comentário.

---

## **Como Rodar o Projeto**

### Pré-requisitos:
- Node.js e npm instalados.

### Passos:
1. Clone o repositório:
   ```bash
   git clone <URL_DO_REPOSITORIO>
Instale as dependências:
bash

npm install
Inicie o servidor de desenvolvimento:


npm start
Acesse o aplicativo em http://localhost:3000.
--
Melhorias Futuras:
---
Implementar rotas para separar melhor as visualizações do menu e dos detalhes.
Adicionar mais funcionalidades, como um formulário para novos comentários.
Melhorar a estilização com temas personalizados do Bootstrap.
Autor
 
* ### Nome: Fulano de Tal
* ### Exercício: UC13 - Aula 13
* ### Data de Conclusão: 02/12/2024