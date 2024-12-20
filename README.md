[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/emy-devfullstack/automation-ceps/blob/main/README.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/emy-devfullstack/automation-ceps/blob/main/README.pt-br.md)

# 📊 Address Data Lookup by ZIP Code (CEP)

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
