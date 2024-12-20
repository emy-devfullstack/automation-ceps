[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/emy-devfullstack/automation-ceps/blob/main/README.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/emy-devfullstack/automation-ceps/blob/main/README.pt-br.md)

# 📊 Busca de Dados de Endereço a partir do CEP

Este script em Python consulta a API pública ViaCEP para buscar informações de logradouro (nome e tipo) a partir de uma lista de CEPs. Ele trata erros, extrai o tipo de logradouro e exibe os resultados no console, além de salvar os dados em um arquivo CSV (`ceps_logradouros.csv`). O script faz uma requisição a cada 0.5 segundos para evitar sobrecarga no servidor.

## Funcionalidades:
- Busca de logradouro e tipo a partir de um CEP.
- Tratamento de erros e resposta padrão para CEPs inválidos.
- Exibição dos resultados no console e gravação em arquivo CSV.

## Como usar:
1. Copie o código.
2. Instale a biblioteca `requests`: `pip install requests`.
3. Execute o script: `python buscar_cep.py`.

### Exemplo de saída no CSV:
```csv
cep,logradouro,tipo_logradouro
32370-670,Rua ABC,Rua
65058-324,Avenida dos Trabalhadores,Avenida
```
---

# Address Data Lookup by ZIP Code (CEP)

This Python script queries the public ViaCEP API to retrieve address information (name and type) from a list of ZIP codes (CEPs). It handles errors, extracts the type of address, and displays the results in the console, as well as saving the data to a CSV file (`ceps_logradouros.csv`). The script makes a request every 0.5 seconds to avoid overloading the server.

## Features:
- Retrieve address and type from a ZIP code (CEP).
- Error handling and default response for invalid ZIP codes.
- Display results in the console and save them to a CSV file.

## How to Use:
1. Copy the code.
2. Install the `requests` library: `pip install requests`.
3. Run the script: `python search_zip.py`.

### Example of CSV Output:
```csv
cep,logradouro,tipo_logradouro
32370-670,Rua ABC,Rua
65058-324,Avenida dos Trabalhadores,Avenida
