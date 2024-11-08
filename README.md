# API ViaCEP

Este projeto é uma API criada em JavaScript para consultar dados do ViaCEP. A API permite que os usuários obtenham informações detalhadas sobre um endereço brasileiro, fornecendo apenas o CEP (Código de Endereçamento Postal).

## Funcionalidades

- **Consulta de CEP**: Busca dados completos de endereço usando apenas o CEP.
- **Formato de Retorno**: Retorna informações em JSON, incluindo logradouro, bairro, cidade, estado, entre outros.
- **Tratamento de Erros**: Validação para CEPs inválidos e tratamento de erros para consultas que não retornam resultados.

## Pré-requisitos

Antes de começar, você precisará ter o [Node.js](https://nodejs.org/) instalado para rodar o projeto.

## Instalação

1. Clone o repositório:

    ```bash
    git clone https://github.com/seu-usuario/api-viacep-js.git
    ```

2. Acesse o diretório do projeto:

    ```bash
    cd api-viacep-js
    ```

3. Instale as dependências:

    ```bash
    npm install
    ```

## Uso

1. Inicie a aplicação:

    ```bash
    npm start
    ```

2. Faça uma requisição para a API com um CEP válido. Exemplo de URL:

    ```
    http://localhost:3000/cep/01001000
    ```

3. A resposta será semelhante a:

    ```json
    {
      "cep": "01001-000",
      "logradouro": "Praça da Sé",
      "complemento": "lado ímpar",
      "bairro": "Sé",
      "localidade": "São Paulo",
      "uf": "SP",
      "ibge": "3550308",
      "gia": "1004",
      "ddd": "11",
      "siafi": "7107"
    }
    ```

## Exemplo de Código

Abaixo está um exemplo de como fazer uma requisição para a API usando JavaScript (Node.js):

```javascript
const axios = require('axios');

async function getAddressByCep(cep) {
    try {
        const response = await axios.get(`http://localhost:3000/cep/${cep}`);
        console.log(response.data);
    } catch (error) {
        console.error('Erro ao buscar o CEP:', error);
    }
}

getAddressByCep('01001000');
