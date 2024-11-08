# ConsultaCEP - Busca de Endereço pelo CEP

Este projeto é uma aplicação simples em HTML e JavaScript para consulta de endereço através do serviço da API ViaCEP. Ao inserir um CEP válido, o sistema busca automaticamente o endereço associado e preenche os campos de endereço no formulário.

## Funcionalidades

- Consulta de endereço a partir do CEP informado.
- Validação do formato de CEP (somente dígitos e no formato válido).
- Mensagens de alerta caso o CEP seja inválido ou não encontrado.

## Tecnologias Utilizadas

- **HTML5**: Estrutura da página.
- **JavaScript**: Lógica de consulta e manipulação do DOM.
- **API ViaCEP**: Serviço para obtenção de dados de endereço a partir de um CEP.

## Estrutura do Projeto

- `index.html`: Contém o código HTML e JavaScript para a aplicação.
- `assets/css/`: Pasta reservada para arquivos CSS (caso adicione estilos no futuro).

## Como Usar

1. Clone este repositório para o seu ambiente local.
2. Abra o arquivo `index.html` em qualquer navegador.
3. Insira um CEP válido no campo de CEP.
4. O endereço será preenchido automaticamente nos campos de formulário.

## Exemplo de Uso

1. Digite um CEP (e.g., `01001000`).
2. Ao sair do campo de CEP, o sistema automaticamente preenche os campos de rua, bairro, cidade, estado e IBGE.

## Requisitos

- Navegador com suporte a JavaScript.

## Créditos

O serviço de consulta de CEP é fornecido pela [API ViaCEP](https://viacep.com.br/).

