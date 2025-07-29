# Testes de Performance com JavaScript e K6

## Introdução

Este repositório contém testes de performance desenvolvidos utilizando JavaScript e a ferramenta K6. O objetivo é simular cargas de usuários em uma API bancária para identificar gargalos e garantir a estabilidade e escalabilidade do sistema. Os testes são configurados para serem executados de forma flexível, permitindo a personalização de variáveis de ambiente para diferentes cenários de teste.



## Tecnologias Utilizadas

*   **JavaScript**: Linguagem de programação utilizada para escrever os scripts de teste.
*   **K6**: Ferramenta de teste de carga e performance de código aberto, focada em desenvolvedores.
*   **Node.js**: Ambiente de execução JavaScript que permite a execução dos scripts de teste fora do navegador.
*   **GJSON**: Para extração de dados em respostas JSON.



## Estrutura do Repositório

O repositório está organizado da seguinte forma:

```
banco-api-performance/
├── config/
├── fixtures/
├── helpers/
├── tests/
├── utils/
├── .gitignore
└── README.md
```




## Objetivo de Cada Grupo de Arquivos

*   `config/`: Contém arquivos de configuração para os testes, como variáveis de ambiente e parâmetros globais.
*   `fixtures/`: Armazena dados de entrada (payloads) utilizados nos testes, como dados de usuários, transações, etc.
*   `helpers/`: Inclui funções auxiliares e módulos reutilizáveis que simplificam a escrita dos scripts de teste.
*   `tests/`: Contém os scripts de teste de performance K6, organizados por funcionalidade ou tipo de teste.
*   `utils/`: Abriga utilitários diversos que podem ser úteis para o projeto, como funções de formatação ou manipulação de dados.




## Modo de Instalação e Execução do Projeto

### Pré-requisitos

Certifique-se de ter o Node.js e o K6 instalados em sua máquina. Você pode baixá-los nos links abaixo:

*   [Node.js](https://nodejs.org/)
*   [K6](https://k6.io/docs/getting-started/installation/)

### Instalação

1.  Clone o repositório:

    ```bash
    git clone https://github.com/andressa-m-ferreira/banco-api-performance.git
    ```

2.  Navegue até o diretório do projeto:

    ```bash
    cd banco-api-performance
    ```


### Execução dos Testes

Para executar os testes, você precisa definir a variável de ambiente `BASE_URL` com a URL base da API que será testada. Além disso, você pode habilitar o dashboard em tempo real do K6 e exportar o relatório HTML.

Exemplo de execução:

```bash
BASE_URL=http://localhost:3000 K6_WEB_DASHBOARD=true K6_WEB_DASHBOARD_EXPORT=html-report.html k6 run tests/seu_teste.js
```

*   Substitua `http://localhost:3000` pela URL da sua API.
*   Substitua `tests/seu_teste.js` pelo caminho do script de teste K6 que você deseja executar.

Após a execução, o relatório HTML estará disponível no arquivo `html-report.html` no diretório raiz do projeto.




