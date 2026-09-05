# 📚 API Testing Automation - Biblioteca (Escola de Devs)

Este projeto demonstra a automação de testes de API ponta a ponta (End-to-End) utilizando o **Postman** para a criação dos cenários, o **Newman** como executor em linha de comando (CLI) e o **GitHub Actions** para a integração contínua (CI/CD).

A API simulada pertence ao repositório da *Escola de Devs* e gerencia o catálogo de livros de uma biblioteca.

## 🧪 Cenários de Testes Automatizados

A coleção do Postman foi estruturada para validar o fluxo principal da API através das seguintes etapas:

1. **Validação de Status da URL:** Garante que o servidor da API está online e respondendo com status HTTP `200 OK`.
2. **Listagem de Livros Disponíveis:** Consulta o catálogo e valida se a API retorna a lista correta de livros cadastrados.
3. **Busca por Tema Específico:** Filtra os livros por um tema/categoria específica e valida se o retorno corresponde ao critério pesquisado.

## 🛠️ Tecnologias e Ferramentas Utilizadas

* **Postman:** Criação, organização e validação dos testes com asserções em JavaScript.
* **Newman:** Executor de testes que permite rodar coleções do Postman direto no terminal.
* **GitHub Actions:** Pipeline de CI/CD configurada para rodar os testes automaticamente a cada `push` ou `pull request` na branch principal.
* **Node.js:** Ambiente de execução necessário para rodar o Newman no fluxo automatizado.

## 🚀 Como Rodar o Projeto Localmente

Se quiser clonar este repositório e executar os testes na sua máquina, siga os passos abaixo:

### Pré-requisitos
Você precisará ter o [Node.js](https://nodejs.org) instalado.

### 1. Instalar o Newman globalmente:
```bash
npm install -g newman
```

### 2. Executar a coleção de testes:
Navegue até a pasta do projeto e execute o comando:
```bash
newman run Biblioteca.postman_collection.json
```

## 🔄 Integração Contínua (CI/CD)

O projeto conta com um fluxo de trabalho automatizado (. GitHub Actions) configurado em `.github/workflows/postman-tests.yml`. 
Sempre que um novo código é enviado para o repositório, o GitHub cria um ambiente virtual, instala as dependências e executa o Newman, garantindo que nenhuma alteração quebre os testes da API.
